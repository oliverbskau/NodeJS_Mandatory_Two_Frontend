
<script>
    import { user } from "../../store/store.js";
    import { Router, Link, Route } from "svelte-navigator";
    import Signup from "../../pages/Signup/Signup.svelte";
import { toasts } from "svelte-toasts";

let username;
let plainTextPassword;



async function handleLogin(){

    const response = await fetch("http://localhost:3000/login", {
        method: 'POST',
        body: JSON.stringify({
            username,
            plainTextPassword

        }),
        headers: {
            "Content-type": "application/json; charset=UTF-8"
        }
    })
    const json = await response.json();
    $user = json.user.username;
    toasts.success(`Logged in as ${$user}`);
} 

function signOut(){
    toasts.success(`${$user} logged out`);
    $user = null;
}

</script>

{#if $user == null}

<div id="formDivLogin">
    
        <input bind:value={username} placeholder="Username" required><br>
        <input bind:value={plainTextPassword} placeholder="Password" type="password" required><br>
        <button on:click={handleLogin} id="sendInfo">Login</button><br>
        <Router>
            <Link to = "/signup"  >Sign up</Link>
        </Router>
        
        <Route path="/signup" component={Signup} />
    
</div>

{:else}

<div id="formDivLoggedIn">
    
    <h2>Logged in as</h2>
    <p>{$user}</p>
    <button on:click={signOut}>Sign out</button>

</div>

{/if}
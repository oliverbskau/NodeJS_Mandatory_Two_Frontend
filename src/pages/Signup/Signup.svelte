

<script>
    import { Router, Link, Route } from "svelte-navigator";
import { toasts } from "svelte-toasts";
import { user } from "../../store/store.js";
   
    
    let username;
    let plainTextPassword;

    async function handleSignup(){
        const response = await fetch("http://localhost:3000/signup", {
        method: 'POST',
        headers: {
            "Content-type": "application/json; charset=UTF-8"
        },
        body: JSON.stringify({
            username,
            plainTextPassword

        }),
       
    })
    const json = await response.json();
    $user = json.user.username;
    toasts.success(`Signed up a new user: ${$user}`);
} 
    


</script>

<div id="formDivSignup">
    
    <input bind:value={username} placeholder="Username" required><br>
    <input bind:value={plainTextPassword} placeholder="Password" type="password" required><br>
    <Router>
    <Link to ="/"> <button on:click={handleSignup} id="sendInfo">Signup</button><br></Link>
        <Link to = "/login"  >Return</Link>
    </Router>
    

</div>
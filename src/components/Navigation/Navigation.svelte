

<script>
	import { Router, Link, Route } from "svelte-navigator";
	import Home from "../../pages/Home/Home.svelte";
    import About from "../../pages/About/About.svelte";
    import Contact from "../../pages/Contact/Contact.svelte";
    import Shop from "../../pages/Shop/Shop.svelte";
    import Cart from "../Cart/Cart.svelte";
    import Login from "../Login/Login.svelte";
    import { user } from "../../store/store.js";
    import Signup from "../../pages/Signup/Signup.svelte";
    import TestPage from "../../pages/TestPage/TestPage.svelte";

    function showCategories(){
            document.getElementById("shopCategories").hidden = false;
            const categoriesNav = document.getElementById("shopCategories");
            categoriesNav.style.margin = "auto";
            categoriesNav.style.marginTop = "100px";
            categoriesNav.style.width = "200px";
   }
   function hideCategories(){
         document.getElementById("shopCategories").hidden = true;
   }

</script>
<div class="topDiv">
<Router>
        <nav id="pagesNav">
            <Link on:click={hideCategories} to="/">Home</Link>
            <Link on:click={showCategories} to="/shop">Shop</Link>
            <Link on:click={hideCategories} to="/about">About</Link>
            <Link on:click={hideCategories} to="/contact">Contact</Link>
            <Link on:click={hideCategories} to="/cart">🛒</Link>
            
            <Link on:click={hideCategories} to="/login">
                {#if $user == null}    
                    Login
                {:else}
                    {$user}
                {/if}
            </Link>
            


        </nav>
    
        <Route path="/about" component={About} />
        <Route path="/contact" component={Contact} />
        <Route path="/shop" component={Shop} />
        <Route path="/" component={Home} />
        <Route path="/login" component={Login} />
        <Route path="/signup" component={Signup} />
        <Route path="/testpage" component={TestPage} />

	
</Router>



</div>


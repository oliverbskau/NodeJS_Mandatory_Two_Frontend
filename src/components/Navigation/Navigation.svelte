

<script>
	import { Router, Link, Route } from "svelte-navigator";
	import Home from "../../pages/Home/Home.svelte";
    import About from "../../pages/About/About.svelte";
    import Contact from "../../pages/Contact/Contact.svelte";
    import Shop from "../../pages/Shop/Shop.svelte";

    function showCategories(){
            const shopLink = document.getElementById("shopCategories").hidden = false;
   }
   function hideCategories(){
            const shopLink = document.getElementById("shopCategories").hidden = true;
   }

</script>
<div class="topDiv">
<Router>





    
        <nav id="pagesNav">
            <Link class="link" on:click={hideCategories} to="/">Home</Link>
            <Link on:click={showCategories} to="/shop">Shop</Link>
            <Link on:click={hideCategories} to="/about">About</Link>
            <Link on:click={hideCategories} to="/contact">Contact</Link>
        </nav>
    
        <Route path="/about" component={About} />
        <Route path="/contact" component={Contact} />
        <Route path="/shop" component={Shop} />
        <Route path="/" component={Home} />

	
</Router>
</div>


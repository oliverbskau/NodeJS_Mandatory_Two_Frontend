

<script>
    import { Router, Link, Route } from "svelte-navigator";
    import Shoes from "../../pages/Shoes/Shoes.svelte";
    import Clothes from "../../pages/Clothes/Clothes.svelte";
    import Electronics from "../../pages/Ëlectronics/Electronics.svelte";
   import Accessories from "../../pages/Accessories/Accesories.svelte";


    function showPagessNav(){
            const menuLink = document.getElementById("pagesNav").hidden = false;
   }
   function hidePagesNav(){
            const menuLink = document.getElementById("pagesNav").hidden = true;
   }
   function returnHome(){
       document.getElementById("shopCategories").hidden = true;
       showPagessNav();
      
   }

 </script>
 



 <Router>
    <nav id="shopCategories" hidden>
        <Link on:click={returnHome} to="/">Home</Link>
        <Link on:click={hidePagesNav} to="/electronics">Electronics</Link>
        <Link on:click={hidePagesNav} to="/clothes">Clothes</Link>
        <Link on:click={hidePagesNav} to="/shoes">Shoes</Link>
        <Link on:click={hidePagesNav} to="/accessories">Accessories</Link>
        
    </nav>

    <Route path="/electronics" component={Electronics} />
    <Route path="/clothes" component={Clothes} />
    <Route path="/shoes" component={Shoes} />
    <Route path="/accessories" component={Accessories} />
 
 </Router>
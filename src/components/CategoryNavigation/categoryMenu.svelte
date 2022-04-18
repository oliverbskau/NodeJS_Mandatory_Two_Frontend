
<script>
    import { Router, Link, Route } from "svelte-navigator";
    function showPagessNav(){
            const menuLink = document.getElementById("pagesNav").hidden = false;
   }
   
   function returnHome(){
       document.getElementById("shopCategories").hidden = true;
       document.getElementById("categoryMenu").hidden = true;
       showPagessNav();
   }
</script>



<Router>
    <div id="categoryMenu" hidden>
    <nav id="categoryMenuNav">
            <Link on:click={returnHome} to="/">Home</Link>
            <Link  to="/electronics">Electronics</Link>
            <Link  to="/clothes">Clothes</Link>
            <Link  to="/shoes">Shoes</Link>
            <Link  to="/accessories">Accessories</Link>
            <Link  to="/cart">🛒</Link>
    </nav>
</div>
 </Router>
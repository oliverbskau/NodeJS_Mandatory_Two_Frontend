

<script>
    import { Router, Link, Route } from "svelte-navigator";
    import Shoes from "../../pages/Shoes/Shoes.svelte";
    import Clothes from "../../pages/Clothes/Clothes.svelte";
    import Electronics from "../../pages/Ëlectronics/Electronics.svelte";
   import Accessories from "../../pages/Accessories/Accesories.svelte";
   import Cart from "../Cart/Cart.svelte";


    function showPagessNav(){
            const menuLink = document.getElementById("pagesNav").hidden = false;
   }
   function hidePagesNav(){
            const menuLink = document.getElementById("pagesNav").hidden = true;
            const categoriesNav = document.getElementById("shopCategories");
            categoriesNav.style.margin = 0;
            categoriesNav.style.width = "100%";
            document.getElementById("shopCategories").hidden = true;
            document.getElementById("categoryMenu").hidden = false;

   }
   function returnHome(){
       document.getElementById("shopCategories").hidden = true;
       document.getElementById("categoryMenu").hidden = true;
       showPagessNav();
   }

 </script>
 



 <Router>
    <div id="shopCategories" hidden>
    <nav id="shopCategoriesNav">
       
            <div class="subCategoryContent" >
            <Link on:click={returnHome} to="/">Home</Link>
        </div>

        <div class="subCategoryContent" >
            <Link on:click={hidePagesNav} to="/electronics">Electronics</Link>
        </div>

        <div class="subCategoryContent" >
            <Link on:click={hidePagesNav} to="/clothes">Clothes</Link>
        </div>

        <div class="subCategoryContent" >
            <Link on:click={hidePagesNav} to="/shoes">Shoes</Link>
        </div>

        <div class="subCategoryContent" >
            <Link on:click={hidePagesNav} to="/accessories">Accessories</Link>
        </div>

        <div class="subCategoryContent" >
            <Link on:click={hidePagesNav} to="/cart">🛒</Link>
        </div>
        
    </nav>
</div>
    <Route path="/electronics" component={Electronics} />
    <Route path="/clothes" component={Clothes} />
    <Route path="/shoes" component={Shoes} />
    <Route path="/accessories" component={Accessories} />
    <Route path="/cart" component={Cart} />
 
 </Router>


 <style>
     .subCategoryContent:hover{
         width: 250px;
     }
 </style>
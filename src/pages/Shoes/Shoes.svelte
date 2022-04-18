


<script>
    import { onMount } from "svelte";
    import Product from "../../components/Product/Product.svelte";
    
    const urlShoes = "http://localhost:3000/shoes";
    let shoesArray = [];
    
    onMount( async() => {
    const response = await fetch(urlShoes);
    const {shoes} = await response.json();
    shoesArray = shoes;
    console.log(shoesArray);
    });
    </script>

<div class="headline">
<h1>Shoes</h1>
</div>

<div class="itemContentWrapper">
{#each shoesArray as shoes}
    <Product item={shoes}/>
{/each}
</div>

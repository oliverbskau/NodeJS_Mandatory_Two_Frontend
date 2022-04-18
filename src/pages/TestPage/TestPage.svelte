


<script>
    import { onMount } from "svelte";
    import Product from "../../components/Product/Product.svelte";
    
    const urlClothes = "http://localhost:3000/clothes";
    let clothesArray = [];
    
    onMount( async() => {
    const response = await fetch(urlClothes);
    const {clothes} = await response.json();
    clothesArray = clothes;
    console.log(clothesArray);
    });
    </script>

<div class="headline">
<h1>TEST PAGE</h1>
</div>

<div class="itemContentWrapper">
{#each clothesArray as clothing}
    <Product item={clothing}/>
{/each}
</div>

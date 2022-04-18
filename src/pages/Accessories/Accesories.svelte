


<script>
    import { onMount } from "svelte";
    import Product from "../../components/Product/Product.svelte";
    
    const urlAccessories = "http://localhost:3000/accessories";
    let accessoriesArray = [];
    
    onMount( async() => {
    const response = await fetch(urlAccessories);
    const {accessories} = await response.json();
    accessoriesArray = accessories;
    console.log(accessoriesArray);
    });
    </script>

<div class="headline">
<h1>Accessories</h1>
</div>

<div class="itemContentWrapper">
{#each accessoriesArray as accessories}
    <Product item={accessories}/>
{/each}
</div>

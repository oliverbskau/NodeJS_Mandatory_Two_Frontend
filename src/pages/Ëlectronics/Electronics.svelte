


<script>
    import { onMount } from "svelte";
    import Product from "../../components/Product/Product.svelte";
    
    const urlElectronics = "http://localhost:3000/electronics";
    let electronicsArray = [];
    
    onMount( async() => {
    const response = await fetch(urlElectronics);
    const {electronics} = await response.json();
    electronicsArray = electronics;
    console.log(electronicsArray);
    });
    </script>

<div class="headline">
<h1>Electronics</h1>
</div>

<div class="itemContentWrapper">
{#each electronicsArray as electronics}
    <Product item={electronics}/>
{/each}
</div>

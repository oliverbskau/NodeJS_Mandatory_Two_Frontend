
<script>
   export let item;

   import { toasts } from "svelte-toasts";

   function addedToCart(){
       console.log(item.name);
       toasts.success(`Added to cart: ${item.name} $${item.price}`);
   }


</script>

<div class="itemContent">
    <h3 class="itemName">{item.name}</h3>
    <h3 class="itemPrice">${item.price}</h3>
    <img id="itemImage" src={"./images/" + item.image} alt='clothingItem' width="250px" height="250px" />
    <p>{item.description}</p>
    
    <button on:click={addedToCart} class="addToCart">Add to cart</button>
    
</div>

<style>

.itemContent{
    width: 300px;
    height: 650px;
    background-color: rgb(247, 244, 244);
    border-radius: 20px;
    border: 5px solid black;
}

.itemContent:hover{
    box-shadow: 0px 10px 10px 10px grey;
}

.itemName{
    font-size: 30px;
    font-family: fantasy;
    letter-spacing: 2px;
    height: 40px;
}

.addToCart{
    background-color: rgb(202, 202, 202);
    padding: 10px 25px;
    border-radius: 15px;
    border: 1px solid black;
    
}

.itemPrice{
    font-size: 25px;
}
</style>
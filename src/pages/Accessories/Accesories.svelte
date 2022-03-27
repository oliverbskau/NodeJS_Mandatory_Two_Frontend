<script>

    let accpic1 = "./images/accpic1.jpg";
    let accpic2= "./images/accpic2.jpg";
    let accpic3 = "./images/accpic3.jpg";
    let accpic4 = "./images/accpic4.webp";
    let accpic5 = "./images/accpic5.jpg";
    
    
    let accessoryItems = [
        {image: accpic1, name: "Thor's Hammer necklace", price: "$100", description: "A necklace for the cool thunder nights" },
        {image: accpic2, name: "Butterfly couple rings", price: "$150", description: "Have a matching ring with your significant other" },
        {image: accpic3, name: "Gangster glasses of fire storm", price: "$10", description: "To the absolute speedster" },
        {image: accpic4, name: "Ikea hat", price: "$5", description: "Go shopping in ikea as a complete professional" },
        {image: accpic5, name: "Oak stone bracelet", price: "$100", description: "It really shouldn't be so expensive, but it is still very cool" }
    ]
    
    </script>

    
    
<div class="headline">
    <h1>Accessories</h1>
</div>

<div class="tableDiv">

    <table>
        <tr>
            <th>Image</th>
            <th>Name</th>
            <th>Price</th>
            <th>Description</th>
            <th>Add</th>
        </tr>
        {#each accessoryItems as accessoryItem}
        <tr>
            <td>
                <img class="tableImg" src={accessoryItem.image} alt="clothingItem"/>
            </td>
            <td>{accessoryItem.name}</td>
            <td>{accessoryItem.price}</td>
            <td>{accessoryItem.description}</td>
            <td>
                <button>Add to cart</button>
            </td>
        </tr>
        {/each}
    </table>

</div>




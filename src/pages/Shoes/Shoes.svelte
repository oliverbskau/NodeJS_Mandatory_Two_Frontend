<script>

    let shoepic1 = "./images/shoepic1.webp";
    let shoepic2 = "./images/shoepic2.webp.crdownload";
    let shoepic3 = "./images/shoepic3.webp";
    let shoepic4 = "./images/shoepic4.webp";
    let shoepic5 = "./images/shoepic5.webp";
    
    
    let shoeItems = [
        {image: shoepic1, name: "Super sneaks", price: "$50", description: "We all know a great shoe, this is also a boot" },
        {image: shoepic2, name: "The boat shoes", price: "$80", description: "Very comfy, very gentleman, very good on a yacht" },
        {image: shoepic3, name: "The agent", price: "$1000", description: "With that price, maybe it has hidden features?" },
        {image: shoepic4, name: "Combat boots", price: "$300", description: "Great all-round boots, for hiking and stuff" },
        {image: shoepic5, name: "Skater-sneaks", price: "$10", description: "Super cheap, destroy them while skating" }
    ]
    
    </script>

    
<div class="headline">
    <h1>Shoes</h1>
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
        {#each shoeItems as shoeItem}
        <tr>
            <td>
                <img class="tableImg" src={shoeItem.image} alt="clothingItem"/>
            </td>
            <td>{shoeItem.name}</td>
            <td>{shoeItem.price}</td>
            <td>{shoeItem.description}</td>
            <td>
                <button>Add to cart</button>
            </td>
        </tr>
        {/each}
    </table>

</div>




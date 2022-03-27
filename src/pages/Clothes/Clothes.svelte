<script>

    let clothespic1 = "./images/clothespic1.jpg";
    let clothespic2= "./images/clothespic2.jpg";
    let clothespic3 = "./images/clothespic3.jpg";
    let clothespic4 = "./images/clothespic4.avif";
    let clothespic5 = "./images/clothespic5.jpg";
    
    
    let clothingItems = [
        {image: clothespic1, name: "T-shirt", price: "$20", description: "Graphic t-shirt with super cool text" },
        {image: clothespic2, name: "Slim fit shirt", price: "$70", description: "Fancy blue shirt that shows off those the great abs" },
        {image: clothespic3, name: "Super coazy long sleeve shirt", price: "$35", description: "For the best coazy days at home in front of the tv" },
        {image: clothespic4, name: "Brow fashables", price: "$10", description: "Hottest pants for fall" },
        {image: clothespic5, name: "Joggedy-walkers", price: "$100", description: "Firm and sturdy hiking pants for long walks" }
    ]
    
    </script>
    
    
    
    <div class="headline">
        <h1>Clothes</h1>
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
            {#each clothingItems as clothingItem}
            <tr>
                <td>
                    <img class="tableImg" src={clothingItem.image} alt="clothingItem"/>
                </td>
                <td>{clothingItem.name}</td>
                <td>{clothingItem.price}</td>
                <td>{clothingItem.description}</td>
                <td>
                    <button>Add to cart</button>
                </td>
            </tr>
            {/each}
        </table>
    
    </div>
    
    
    
    
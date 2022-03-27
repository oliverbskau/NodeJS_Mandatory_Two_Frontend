<script>

let elecpic1 = "./images/elecpic1.jpg";
let elecpic2 = "./images/elecpic2.webp";
let elecpic3 = "./images/elecpic3.jpg";
let elecpic4 = "./images/elecpic4.webp";
let elecpic5 = "./images/elecpic5.webp";


let electronicalItems = [
    {image: elecpic1, name: "Kea Super Computer v3", price: "$1000", description: "Testwinning computer for larger coding projects" },
    {image: elecpic2, name: "Stretchy-lab-top", price: "$560", description: "The new stretchy labtop from kea-ware" },
    {image: elecpic3, name: "PS5 controller", price: "$103", description: "The best and most immersive gaming controller" },
    {image: elecpic4, name: "Nintendo Switch", price: "$299", description: "The best portable family gaming console" },
    {image: elecpic5, name: "Flippedy-flop-phone", price: "$900", description: "Why not bottle-flip the new flippy-phone? Always lands perfect" }
]

</script>



<div class="headline">
    <h1>Electronics</h1>
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
        {#each electronicalItems as electronicalItem}
        <tr>
            <td>
                <img class="tableImg" src={electronicalItem.image} alt="electronicalItem"/>
            </td>
            <td>{electronicalItem.name}</td>
            <td>{electronicalItem.price}</td>
            <td>{electronicalItem.description}</td>
            <td>
                <button>Add to cart</button>
            </td>
        </tr>
        {/each}
    </table>

</div>




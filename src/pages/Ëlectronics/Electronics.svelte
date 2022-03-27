<script>

let electronicalItems = [
    {image: "testImage1", name: "testName", price: "testPrice", description: "testDescription" },
    {image: "testImage2", name: "testName", price: "testPrice", description: "testDescription" },
    {image: "testImage3", name: "testName", price: "testPrice", description: "testDescription" },
    {image: "testImage4", name: "testName", price: "testPrice", description: "testDescription" },
    {image: "testImage5", name: "testName", price: "testPrice", description: "testDescription" }
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
            <td>{electronicalItem.image}</td>
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




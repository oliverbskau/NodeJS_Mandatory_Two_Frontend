
<script>
    import SliderGalery from "simple-svelte-slideshow";

    let clothesPicture = "./clothes.jpg";
    let electronicsPicture = "./electronic-gadgets.jpeg";
    let shoesPicture ="./shoes.jpg";
    let accesoriesPicture ="./accesories.jpg"

    let imgArray = [
        {src: clothesPicture, text: "Clothes"},
        {src: electronicsPicture, text: "Electronics"},
        {src: shoesPicture, text: "Shoes"},
        {src: accesoriesPicture, text: "Accessories"}
    ]
    const easingMethod = "sineInOut";
    const duration = 1000;
</script>



<div class="headline">
    <h1>Home</h1>
</div>

<div class="content">
    <SliderGalery class="slider" {imgArray} {duration} {easingMethod} />
</div>



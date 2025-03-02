<div id="carousel-container" style="text-align: center; position: relative; max-width: 600px; margin: auto;">
    <img id="carousel-image" src="img/carousel/image1.png" alt="Carosello" style="width: 100%; border-radius: 10px;">
    
    <button id="prev-button" style="position: absolute; left: 0; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10094;</button>
    <button id="next-button" style="position: absolute; right: 0; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10095;</button>
</div>

<script>
    const images = [
        "img/pokemon/abra.png",
        "img/pokemon/kadabra.png",
        "img/pokemon/alakazam.png"
    ];
    
    let currentIndex = 0;
    const imageElement = document.getElementById("carousel-image");
    const prevButton = document.getElementById("prev-button");
    const nextButton = document.getElementById("next-button");

    prevButton.addEventListener("click", () => {
        currentIndex = (currentIndex - 1 + images.length) % images.length;
        imageElement.src = images[currentIndex];
    });

    nextButton.addEventListener("click", () => {
        currentIndex = (currentIndex + 1) % images.length;
        imageElement.src = images[currentIndex];
    });
</script>

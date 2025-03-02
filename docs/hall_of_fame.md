<div id="carousel-container" style="text-align: center; position: relative; max-width: 600px; margin: auto;">
    <img id="carousel-image" src="img/types/special.png" alt="Tipo Speciale" style="width: 100%; border-radius: 10px;">
    
    <button id="prev-button" style="position: absolute; left: 0; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10094;</button>
    <button id="next-button" style="position: absolute; right: 0; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10095;</button>
</div>

<script>
    const images = [
        "img/types/special.png",
        "img/types/physical.png",
        "img/types/status.png"
    ];
    
    let currentIndex = 0;
    const imageElement = document.getElementById("carousel-image");
    const prevButton = document.getElementById("prev-button");
    const nextButton = document.getElementById("next-button");

    function updateImage() {
        imageElement.outerHTML = `<img id="carousel-image" src="${images[currentIndex]}" alt="Carosello" style="width: 100%; border-radius: 10px;">`;
    }

    prevButton.addEventListener("click", () => {
        currentIndex = (currentIndex - 1 + images.length) % images.length;
        updateImage();
    });

    nextButton.addEventListener("click", () => {
        currentIndex = (currentIndex + 1) % images.length;
        updateImage();
    });
</script>
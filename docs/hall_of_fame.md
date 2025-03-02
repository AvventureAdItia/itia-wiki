<div class="slideshow-container">
    <div class="slide">
        <img src="img/types/special.png" alt="Tipo Speciale">
    </div>
    <div class="slide">
        <img src="img/types/physical.png" alt="Tipo Fisico">
    </div>
    <div class="slide">
        <img src="img/types/status.png" alt="Tipo Stato">
    </div>
</div>

<style>
    .slideshow-container {
        display: flex;
        overflow: hidden;
        max-width: 600px;
    }

    .slide {
        animation: slideAnimation 6s infinite;
        min-width: 100%;
    }

    @keyframes slideAnimation {
        0% { transform: translateX(0); }
        33% { transform: translateX(-100%); }
        66% { transform: translateX(-200%); }
        100% { transform: translateX(0); }
    }
</style>

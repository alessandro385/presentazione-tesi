/* Background con immagine della lampadina come sfondo principale */
        .background-wrapper {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
        }

        .background-image {
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: 65% 45%;
            transform: scale(0.7);
            image-rendering: -webkit-optimize-contrast;
            image-rendering: crisp-edges;
        }

        /* Overlay gradiente per dare profondità e leggibilità */
        .background-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                to right,
                rgba(10, 25, 47, 0.88) 0%,
                rgba(10, 25, 47, 0.65) 35%,
                rgba(10, 25, 47, 0.2) 60%,
                rgba(10, 25, 47, 0.5) 100%
            );
        }
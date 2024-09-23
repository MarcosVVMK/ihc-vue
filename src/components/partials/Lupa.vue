<template>
    <div class="lupa-container w-8 h-8" @mousemove="moveLupa" @mouseleave="hideLupa">
      <img src="../../assets/images/lupa.png" alt="Imagem para zoom" class="imagem-zoom" />
      <div v-if="isZoomed" class="lupa" :style="lupaStyle"></div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isZoomed: false,
        lupaStyle: {
          backgroundImage: '',
          backgroundSize: '200%', // Tamanho do zoom
          backgroundPosition: 'center',
          width: '100px', // Tamanho da lupa
          height: '100px',
          borderRadius: '50%',
          position: 'absolute',
          pointerEvents: 'none', // Para não bloquear eventos
          display: 'none',
        },
      };
    },
    methods: {
      moveLupa(event) {
        const img = event.target.querySelector('.imagem-zoom');
        const rect = img.getBoundingClientRect();
        const x = event.clientX - rect.left; // Posição X do mouse
        const y = event.clientY - rect.top; // Posição Y do mouse
  
        this.lupaStyle.backgroundImage = `url(${img.src})`;
        this.lupaStyle.backgroundPosition = `${(x / rect.width) * 100}% ${(y / rect.height) * 100}%`;
        this.lupaStyle.left = `${event.clientX - 50}px`; // Centraliza a lupa
        this.lupaStyle.top = `${event.clientY - 50}px`;
        this.lupaStyle.display = 'block';
        this.isZoomed = true;
      },
      hideLupa() {
        this.isZoomed = false;
        this.lupaStyle.display = 'none';
      },
    },
  };
  </script>
  
  <style>
  .lupa-container {
    position: relative;
    display: inline-block;
  }
  
  .imagem-zoom {
    width: 500px; /* Ajuste o tamanho da imagem */
    height: auto;
  }
  
  .lupa {
    border: 2px solid #000;
    opacity: 0.7;
    pointer-events: none;
    transition: display 0.1s;
  }
  </style>
  
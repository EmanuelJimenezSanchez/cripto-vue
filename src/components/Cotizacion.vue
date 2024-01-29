<script setup>
  const props = defineProps({
    cotizacion: {
      type: Object,
      required: true
    }
  })
</script>

<template>
  <div 
    class="contenedor-resultado"
  >
    <h2>Cotizacion</h2>

    <div class="resultado">
      <img 
        :src="'https://cryptocompare.com/' + cotizacion.IMAGEURL" 
        alt="imagen cript"
      >

      <div>
        <p>El precio es de: <span>{{ cotizacion.PRICE }}</span></p>
        <p>Precio mas alto del dia: <span>{{ cotizacion.HIGHDAY }}</span></p>
        <p>Variacion ultimas 24 horas: <span>{{ cotizacion.CHANGEPCT24HOUR }}%</span></p>
        <p>Ultima actualizacion: <span>{{ cotizacion.LASTUPDATE }}</span></p>
      </div>
    </div>
  </div>
</template>


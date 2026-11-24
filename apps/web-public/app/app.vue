<script setup lang="ts">
const open=ref(false)
const links=[{label:'Formación',to:'/#formacion'},{label:'Formación bonificada',to:'/formacion-bonificada'},{label:'Para empresas',to:'/#empresas'},{label:'Preguntas frecuentes',to:'/#preguntas'}]
</script>
<template>
<a class="skip" href="#contenido">Saltar al contenido</a>
<header class="header"><div class="wrap nav"><NuxtLink to="/" class="brand" aria-label="PIRO Academy, inicio"><span class="mark" aria-hidden="true">▷</span><span>PIRO<small>ACADEMY</small></span></NuxtLink><button class="menu" :aria-expanded="open" aria-controls="navigation" @click="open=!open">Menú</button><nav id="navigation" :class="{open}" aria-label="Principal"><NuxtLink v-for="link in links" :key="link.to" :to="link.to" @click="open=false">{{link.label}}</NuxtLink><a class="outline" href="https://empresas.gestionapymes.es">Área de empresas</a><a class="button" href="https://campus.gestionapymes.es">Campus</a></nav></div></header>
<main id="contenido"><NuxtPage /></main>
<footer><div class="wrap foot"><div><strong>PIRO Academy</strong><p>Formación para empresas · GestionaPymes.es</p></div><div><NuxtLink to="/formacion-bonificada">Formación bonificada</NuxtLink><NuxtLink to="/cursos/marketing-digital-ia">Programa formativo</NuxtLink></div><p>Web en preparación. Matrículas todavía no disponibles.</p></div></footer>
</template>
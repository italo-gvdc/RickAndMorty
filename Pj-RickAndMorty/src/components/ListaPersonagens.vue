<script setup>
const props = defineProps(["character"])
</script>

<template>
  <div class="col-md-4">
    <div class="card p-2 mb-3">
      <img :src="character.image" height="auto" alt="">
      <div class="card-body">
        <p class="text-center"><strong>Nome: {{ character.name }}</strong></p>
        <p>Status: {{ character.status }}</p>
        <p>Espécie: {{ character.species }}</p>
        <p>Genero: {{ character.gender }}</p>
        <p>Localização: {{ character.location.name }}</p>
        <p>Episódios: {{ character.episode.length }}</p>
      </div>
    </div>
  </div>
</template>

<style>
.card {
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.3s ease;
}

.card:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}


.card-img-top {
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}


.card-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
}


.character-info {
  margin-top: 20px;
}

.character-info p {
  margin-bottom: 10px;
}

.character-info span {
  font-weight: bold;
}
</style>

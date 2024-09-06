<template>
  <v-card
    class="card-sort mx-auto w-100" 
    width="auto"
  >
    <v-tooltip text="Сортировка по рейтингу(по возрастанию)">
      <template v-slot:activator="{ props }">
        <v-btn
        v-bind="props"
        icon="mdi-sort-ascending"
        density="compact"
        variant="tonal"
        class="sort-btn"
        color="blue"
        @click="$emit('change', options.asc)" />
      </template>
    </v-tooltip>
    <v-tooltip text="Сортировка по рейтингу(по убыванию)">
      <template v-slot:activator="{ props }">
        <v-btn
        v-bind="props"
        icon="mdi-sort-descending"
        density="compact"
        variant="tonal"
        class="sort-btn"
        color="green"
        @click="$emit('change', options.desc)" />
      </template>
    </v-tooltip>
    <v-tooltip text="Сортировка по рейтингу (без сортировки)">
      <template v-slot:activator="{ props }">
        <v-btn
          v-bind="props"
          icon="mdi-sort-variant-remove"
          density="compact"
          variant="tonal"
          class="sort-btn"
          color="red"
          @click="$emit('change', options.without)" />
      </template>
    </v-tooltip>
  </v-card>
</template>
<script setup>
  const props = defineProps({
    options: {},
  });
</script>
<style lang="scss" scoped>
  .card-sort {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 20px;
    padding: 5% 10%;
    width: 100%;
    background-color: rgb(255, 255, 255);
    border-radius: 10px;
    position: relative;
  }
</style>
<template>
    <div>
        <h1>
            {{ species }} for adoption
        </h1>
        <b-table striped hover :items="pets">
            <template #cell(name)="data">
                <router-link :to="`/pets/cats/${species}`">{{ data.value }}</router-link>
            </template>
        </b-table>
    </div>
</template>

<script>
export default {
  props: {
    species: String,
    pets: Array
  }
}
</script>

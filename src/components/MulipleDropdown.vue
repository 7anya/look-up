<template>
<!-- <h5>Yeet</h5> -->
  <div class="md-layout md-gutter">

    <div class="md-layout-item">
      <md-field>
        <label for="movies">{{title}}</label>
        <md-select v-model="selectedOptions" name="movies" id="movies" >
        <!-- <div :key="item" v-for="item in allOptions">
          <md-option value="item">{{item}}</md-option>
        </div>  -->
          <md-option value="fight-club">Fight Club</md-option>
          <md-option value="godfather">Godfather</md-option>
          <md-option value="godfather-ii">Godfather II</md-option>
          <md-option value="godfather-iii">Godfather III</md-option>
          <md-option value="godfellas">Godfellas</md-option>
          <md-option value="pulp-fiction">Pulp Fiction</md-option>
          <md-option value="scarface">Scarface</md-option>
        </md-select>
      </md-field>

      <div>
        <strong>Selected Options:</strong>
        {{ selectedOptions }}
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'MultipleSelect',
    props: {
      title: String,
      options: Array
    },
    
    data: () => ({
      allOptions:  ["one", "two", "three"],
      selectedOptions: ""
    })
  }
</script>

<style lang="scss" scoped>
  .md-field {
    max-width: 300px;
  }
</style>
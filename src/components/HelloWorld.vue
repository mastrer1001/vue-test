<template>
  <div>
    <h1>{{ message }}</h1>
    <p>
      {{intro}}
    </p>
    <div v-if = "vorgehenButtonClicked===false">
    <h3>Zutaten</h3>
    <ul>
      <li v-for= "item in zutaten" :key="item.zutat">
        {{item.zutat}}
      </li>
    </ul>
    </div>
    <div v-else>
    <h3>Vorgehen</h3>
    <ul>
      <li v-for= "step in vorgehen" :key="step.schritt">
        {{step.schritt}}
      </li>
    </ul>
    </div>
    <div class="btn-group">
      <button v-on:click = "vorgehenButtonClicked = false">Zutaten</button>
      <button v-on:click = "vorgehenButtonClicked = true">Vorgehen</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    message: String,
    intro: String,
  },
  data(){
    return{
      vorgehenButtonClicked: Boolean,
      zutaten:[
        {zutat: '200g Spagetti'},
        {zutat: '50g Parmesan, gerieben'},
        {zutat: '150g Pancetta oder Schinken'},
        {zutat: '2 Eier'},
        {zutat: 'Salz'},
        {zutat: 'Pfeffer'},
      ],
      vorgehen:[
        {schritt: 'Spagetti in kochendem Salzwasser kochen'},
        {schritt: 'In der Zwischenzeit Pancetta anbraten bis das Fett ausgelaufen ist'},
        {schritt: 'Eier mit dem Parmesan und reichlich Pfeffer verquirlen'},
        {schritt: 'Pancetta aus der Pfanne entfernen und Hitze auf niedrig stellen'},
        {schritt: 'Die Spagetti sobald sie fertig sind abgießen und mit dem Fett in der Pfanne vermengen'},
        {schritt: 'Pancetta und Eimischung zügig in die Pfanne geben und verrühren, dabei darauf achten, dass die Eier nicht zu viel kochen. Die Pfanne sollte nicht mehr auf der Herdplatte sein müssen, das Kochen geschieht durch die Hitze der Nudeln.'},
        {schritt: 'So schnell wie möglich servieren'},
      ],
    }
  },
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
  text-align: center;
}
li {
  display: block;
  margin-top: 10px;
}
a {
  color: #cca01f;
}
.btn-group{
  width:30%;
  margin-left: auto;
  margin-right: auto;
}
.btn-group button{
  width:50%;
  min-width: fit-content;
  text-align: center;
  background-color: #cca01f;
  border: 1px solid #864f09; /* Green border */
  color: white; /* White text */
  padding: 10px 24px; /* Some padding */
  cursor: pointer; /* Pointer/hand icon */
  float: left; /* Float the buttons side by side */
}

.btn-group button:not(:last-child) {
  border-right: none; /* Prevent double borders */

}
.btn-group button:hover {
  background-color: #49371f;
}
</style>
<!-- Add "scoped" attribute to limit CSS to this component only -->

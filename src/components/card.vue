<script setup>
import { defineProps, ref } from 'vue';
const props = defineProps(['data'])
const data = props.data
const isVisible = ref(false)
const toggleVisibility = () => {
  isVisible.value = !isVisible.value;
};
</script>

<template>
  <div class="card" @click="toggleVisibility">
    <div class="card-item" v-if="isVisible === false">
      <img :src="data.img" alt="" />
      <h5>{{ data.name }}</h5>
    </div>
    <div v-if="isVisible === true" class="back">
      <ul>
        <li v-for="(option, index) in data.options" :key="index">
          {{ option }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style>
.card {
  border:#003366 solid;
  margin: 5px;
  padding-top: 15px;
  width: 200px;
  height: 120px;
  border-radius: 15px; 
  background-color: #E9F6FF;
  color: black;
 
}
.card:hover{
   box-shadow: rgba(0, 0, 0, 0.631) 3px 5px;
}

.card-item{
  margin-top: 5px; 
}

.card-item img{
  width: 3em;

}
.card:hover img{
  transform: scale(1.5);
}
</style>
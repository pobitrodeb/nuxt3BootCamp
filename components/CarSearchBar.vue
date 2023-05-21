<script setup>
  const city = ref(''); 
  const cityError = ref(false); 

  const handleSearch = () => {
      if(!city.value){
        return cityError.vue = true 
      }
    navigateTo(`/city/${city.value}/car/`);
  }

</script>


<template>
  <!-- ------ Home Search Bar ------  -->
  <div
    class="font-serif w-100[px] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto"
  >
    <input
      type="text"
      class="py-3 px-5 w-full text-2xl rounded-4 focus:outline-none"
      placeholder="search by city.."
      v-model="city"
      :class=" cityError ? 'border-red-500 border' : '' "
    />
    <button class="bg-sky-500 px-10 text-white" @click="handleSearch">Search</button>
  </div>
  <!-- ------ Home Search Bar ------  -->
</template>
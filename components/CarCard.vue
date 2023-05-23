<script setup>
  const props = defineProps({
      car: Object, 
  })
</script>

<template>
     <!-- CAR CARD -->
     <div
        class="shadow border w-full overflow-hidden mb-5 cursor-pointer h-[200px]"
        @click="navigateTo(`/car/${car.name}-${car.id}`)"
      >
      <!-- @click="navigateTo(`/car/${car.name}-${car.id}`)" -->
        <div class="flex h-full">
          <!-- {{ car }} -->
          <!-- <img :src="car.url" alt=""> -->
          <img
            src="https://carwow-uk-wp-3.imgix.net/Volvo-XC40-white-scaled.jpg"
            alt=""
            class="w-[300px] h-full"
          />
          <div class="p-4 flex flex-col">
            <div>
              <!-- <h1 class="text-2xl text-blue-700">{{ car.name }}</h1> -->
              <h1 class="text-2xl text-blue-700">Volvo XC40</h1>
              <!-- <p class="text-gray-700">
                {{ car.description }}
              </p> -->
              <p class="text-gray-700">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
            </div>
            <!-- <h1 class="mt-auto text-xl">{{ car.price }}</h1> -->
            <h1 class="mt-auto text-xl">$39,555</h1>
          </div>
        </div>
      </div>
      <!-- CAR CARD -->
</template>
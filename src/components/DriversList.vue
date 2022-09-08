<template>
  <div>
    <h1 class="text-3xl font-bold underline p-8">Drivers</h1>
    <ul class="flex flex-wrap justify-items-between">
      <li
        v-for="(driver, index) in drivers"
        :key="index"
        class="w-full md:w-72 min-h-32 mx-4 my-12"
      >
        <div
          class="
            md:w-72
            h-full
            bg-gray-200
            rounded
            flex flex-col
            text-center
            flex
          "
        >
          <span class="mx-auto"
            ><img
              v-if="driver.photo"
              :src="driver.photo"
              :alt="driver.name"
              class="rounded-full -my-12 border-2 border-white w-28" />
            <img
              v-else
              src="@/assets/user.png"
              :alt="driver.name"
              class="rounded-full -my-12 border-2 border-white w-28"
          /></span>
          <div class="flex flex-col mt-12 p-6">
            <span class="font-bold text-xl">{{ driver.name }}</span>
            <span>{{ driver.licenceNo }}</span>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DriversList",
  props: {
    drivers: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

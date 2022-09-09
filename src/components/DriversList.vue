<template>
  <div class="relative">
    <h1 class="text-3xl font-bold underline p-8">Drivers</h1>
    <ul class="flex flex-wrap justify-items-between w-full mx-auto">
      <li
        v-for="driver in drivers"
        :key="driver.id"
        @click="showDriverInfo(driver)"
        class="w-full md:w-72 min-h-32 mx-4 my-12 cursor-pointer"
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
            <div v-if="driver.vehicle">
              <img
                src="@/assets/taxi.svg"
                :alt="driver.name"
                class="rounded-full mx-auto w-8 border-2 border-white bg-white"
              />
            </div>
          </div>
        </div>
      </li>
    </ul>
    <div
      v-if="selectedDriver.length"
      class="selected h-screen w-screen bg-gray-500/40 fixed inset-0"
    >
      <div
        class="
          selected
          h-1/2
          md:w-1/2
          w-3/4
          bg-gray-500
          container
          transition
          duration-150
          fade-in
          rounded
          md:px-12
          px-4
          mx-auto
          md:my-12
          my-6
          text-white
        "
      >
        <div
          @click="closeModal"
          class="cursor-pointer py-6 text-yellow-500 text-right"
        >
          Close
        </div>
        <div class="flex flex-col md:flex-row justify-between w-full">
          <h2 class="text-2xl text-left">
            <span class="text-gray-300">Name:</span>
            {{ selectedDriver[0].name }}
          </h2>
          <p class="md:text-right">
            <span class="text-gray-300 flex flex-col">Licence Number:</span
            >{{ selectedDriver[0].licenceNo }}
          </p>
        </div>
        <div v-if="selectedDriver[0].vehicle">
          <h2 class="text-2xl text-left text-gray-300 mb-2">Vehicle:</h2>
          <h3 class="text-xl text-left">
            {{ selectedDriver[0].vehicle.make }}<br />
            {{ selectedDriver[0].vehicle.model }}<br />
            {{ selectedDriver[0].vehicle.registation }}<br />
            {{ selectedDriver[0].vehicle.dateLastDriven }}<br />
          </h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DriversList",
  props: {
    drivers: Array,
  },
  data() {
    return {
      selectedDriver: [],
    };
  },
  methods: {
    showDriverInfo(driver) {
      var index = this.selectedDriver.findIndex(
        (item) => item.id === driver.id
      );

      if (index === -1) {
        this.selectedDriver.push(driver);
      } else {
        this.selectedDriver.splice(index, 1);
      }
    },
    closeModal() {
      this.selectedDriver = [];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

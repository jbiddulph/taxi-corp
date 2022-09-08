<template>
  <div>
    <h1 class="text-3xl font-bold underline p-8">Users</h1>
    <ul class="flex flex-wrap justify-items-between">
      <li
        v-for="user in users"
        :key="user.id"
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
              v-if="user.photo"
              :src="user.photo"
              :alt="user.name"
              class="rounded-full -my-12 border-2 border-white w-28" />
            <img
              v-else
              src="@/assets/user.png"
              :alt="user.name"
              class="rounded-full -my-12 border-2 border-white w-28"
          /></span>
          <div class="flex flex-col mt-12 p-6">
            <span class="font-bold text-xl">{{ user.name }}</span>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TestList",
  props: {
    users: Array,
  },
};
</script>
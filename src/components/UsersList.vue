<template>
  <div>
    <h1 class="text-3xl font-bold underline p-8">Users</h1>
    <ul class="flex flex-wrap justify-items-between">
      <li
        v-for="user in users"
        :key="user.id"
        @click="showUserInfo(user)"
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
    <div
      v-if="selectedUser.length"
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
        <div class="flex flex-col md:flex-row w-full">
          <h2 class="text-2xl text-left">
            {{ selectedUser[0].name }}
          </h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TestList",
  props: {
    users: Array,
  },
  data() {
    return {
      selectedUser: [],
    };
  },
  methods: {
    showUserInfo(user) {
      var index = this.selectedUser.findIndex((item) => item.id === user.id);

      if (index === -1) {
        this.selectedUser.push(user);
      } else {
        this.selectedUser.splice(index, 1);
      }
    },
    closeModal() {
      this.selectedUser = [];
    },
  },
};
</script>
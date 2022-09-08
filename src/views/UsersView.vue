<template>
  <div v-if="loadedUsers" class="container mx-auto w-full">
    <UsersList :users="usersInfo" />
  </div>
</template>

<script>
import UsersList from "@/components/UsersList.vue";

export default {
  name: "UsersList",
  components: {
    UsersList,
  },
  data() {
    return {
      loadedUsers: false,
      usersInfo: [
        {
          id: 1,
          name: "Justin Hughes",
          photo: "https://randomuser.me/api/portraits/men/21.jpg",
        },
        {
          id: 2,
          name: "Amanda Johnson",
          photo: "https://randomuser.me/api/portraits/women/22.jpg",
        },
        {
          id: 3,
          name: "Andrew Price",
          photo: "https://randomuser.me/api/portraits/men/23.jpg",
        },
        {
          id: 4,
          name: "Isla Collins",
          photo: "https://randomuser.me/api/portraits/women/24.jpg",
        },
        {
          id: 5,
          name: "Margaret Turner",
          photo: "https://randomuser.me/api/portraits/women/25.jpg",
        },
        {
          id: 6,
          name: "Patrick Kelly",
          photo: "https://randomuser.me/api/portraits/men/26.jpg",
        },
        {
          id: 7,
          name: "Laura Wood",
          photo: "https://randomuser.me/api/portraits/women/27.jpg",
        },
        {
          id: 8,
          name: "Jose Wright",
          photo: "https://randomuser.me/api/portraits/men/28.jpg",
        },
        {
          id: 9,
          name: "Charlie Edwards",
          photo: "https://randomuser.me/api/portraits/men/29.jpg",
        },
        {
          id: 10,
          name: "Janet Turner",
          photo: "",
        },
        {
          id: 11,
          name: "Eric Moore",
          photo: "https://randomuser.me/api/portraits/men/31.jpg",
        },
        {
          id: 12,
          name: "Carolyn Thompson",
          photo: "",
        },
        {
          id: 13,
          name: "Barbara Wood",
          photo: "https://randomuser.me/api/portraits/women/33.jpg",
        },
        {
          id: 14,
          name: "David Anderson",
          photo: "https://randomuser.me/api/portraits/men/34.jpg",
        },
        {
          id: 15,
          name: "Nicole Clarke",
          photo: "https://randomuser.me/api/portraits/women/35.jpg",
        },
        {
          id: 16,
          name: "Brenda Wilson",
          photo: "https://randomuser.me/api/portraits/women/36.jpg",
        },
        {
          id: 17,
          name: "Kenneth Phillips",
          photo: "",
        },
        {
          id: 18,
          name: "Michelle Hill",
          photo: "https://randomuser.me/api/portraits/women/38.jpg",
        },
      ],
    };
  },
  mounted() {
    this.loadedUsers = true;
  },
};
</script>

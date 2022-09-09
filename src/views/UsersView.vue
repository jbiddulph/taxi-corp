<template>
  <div v-if="loadedUsers" class="container mx-auto w-full">
    <UsersList :users="usersInfo" />
  </div>
</template>

<script>
import UsersList from "@/components/UsersList.vue";

export default {
  name: "UserView",
  components: {
    UsersList,
  },
  data() {
    return {
      loadedUsers: false,
      usersInfo: [
        {
          id: 1,
          name: "Gilbert Kennedy",
          photo: "https://randomuser.me/api/portraits/men/21.jpg",
        },
        {
          id: 2,
          name: "Justine Smith",
          photo: "",
        },
        {
          id: 3,
          name: "Ralph Graves",
          photo: "https://randomuser.me/api/portraits/men/23.jpg",
        },
        {
          id: 4,
          name: "Violet Porter",
          photo: "https://randomuser.me/api/portraits/women/24.jpg",
        },
        {
          id: 5,
          name: "Haley Read",
          photo: "",
        },
        {
          id: 6,
          name: "Lucas Elledge",
          photo: "https://randomuser.me/api/portraits/men/26.jpg",
        },
        {
          id: 7,
          name: "Trina Hardy",
          photo: "https://randomuser.me/api/portraits/women/27.jpg",
        },
        {
          id: 8,
          name: "Adele Reid",
          photo: "https://randomuser.me/api/portraits/men/28.jpg",
        },
        {
          id: 9,
          name: "Winston Matthews",
          photo: "https://randomuser.me/api/portraits/men/29.jpg",
        },
        {
          id: 10,
          name: "Bailey Fennimore",
          photo: "",
        },
        {
          id: 11,
          name: "Zeph King",
          photo: "https://randomuser.me/api/portraits/men/31.jpg",
        },
        {
          id: 12,
          name: "Regina Dawson",
          photo: "",
        },
        {
          id: 13,
          name: "Elaine Skinner",
          photo: "https://randomuser.me/api/portraits/women/33.jpg",
        },
        {
          id: 14,
          name: "Daley Gilbert",
          photo: "https://randomuser.me/api/portraits/men/34.jpg",
        },
        {
          id: 15,
          name: "Katherine Schuman",
          photo: "https://randomuser.me/api/portraits/women/35.jpg",
        },
        {
          id: 16,
          name: "Miranda Martin",
          photo: "https://randomuser.me/api/portraits/women/36.jpg",
        },
        {
          id: 17,
          name: "Tony Sandoval",
          photo: "",
        },
        {
          id: 18,
          name: "Rowena Lawson",
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

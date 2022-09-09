<template>
  <div v-if="loadedDrivers" class="container mx-auto w-full">
    <DriversList :drivers="driversInfo" />
  </div>
</template>

<script>
import DriversList from "@/components/DriversList.vue";

export default {
  name: "HomeView",
  components: {
    DriversList,
  },
  data() {
    return {
      loadedDrivers: false,
      driversInfo: [
        {
          id: 1,
          name: "Justin Hughes",
          photo: "https://randomuser.me/api/portraits/men/1.jpg",
          licenceNo: "JH-567567689",
          vehicle: {
            registation: "AB22JMB",
            make: "VW",
            model: "Golf",
            dateLastDriven: "07-09-2022",
          },
        },
        {
          id: 2,
          name: "Amanda Johnson",
          photo: "https://randomuser.me/api/portraits/women/2.jpg",
          licenceNo: "AJ-76687688",
          vehicle: {
            registation: "HG21XYZ",
            make: "VW",
            model: "Jetta",
            dateLastDriven: "09-09-2022",
          },
        },
        {
          id: 3,
          name: "Andrew Price",
          photo: "https://randomuser.me/api/portraits/men/3.jpg",
          licenceNo: "AP-8765432",
          vehicle: {
            registation: "T4X1",
            make: "FORD",
            model: "CAPRI",
            dateLastDriven: "09-09-2022",
          },
        },
        {
          id: 4,
          name: "Isla Collins",
          photo: "https://randomuser.me/api/portraits/women/4.jpg",
          licenceNo: "IC-09099876",
          vehicle: {
            registation: "AU69FTY",
            make: "AUDI",
            model: "A3",
            dateLastDriven: "04-09-2022",
          },
        },
        {
          id: 5,
          name: "Margaret Turner",
          photo: "https://randomuser.me/api/portraits/women/5.jpg",
          licenceNo: "MT-22265557",
        },
        {
          id: 6,
          name: "Patrick Kelly",
          photo: "https://randomuser.me/api/portraits/men/6.jpg",
          licenceNo: "PK-1144554",
        },
        {
          id: 7,
          name: "Laura Wood",
          photo: "https://randomuser.me/api/portraits/women/7.jpg",
          licenceNo: "LW-3434234",
        },
        {
          id: 8,
          name: "Jose Wright",
          photo: "https://randomuser.me/api/portraits/men/8.jpg",
          licenceNo: "JW-998765",
        },
        {
          id: 9,
          name: "Charlie Edwards",
          photo: "https://randomuser.me/api/portraits/men/9.jpg",
          licenceNo: "CE-8887756",
          vehicle: {
            registation: "HJ51JMB",
            make: "Mercedes",
            model: "AMG 45",
            dateLastDriven: "07-09-2022",
          },
        },
        {
          id: 10,
          name: "Janet Turner",
          photo: "",
          licenceNo: "JT-555666",
        },
        {
          id: 11,
          name: "Eric Moore",
          photo: "https://randomuser.me/api/portraits/men/11.jpg",
          licenceNo: "EM-766222688",
          vehicle: {
            registation: "A21BMW",
            make: "BMW",
            model: "M3",
            dateLastDriven: "08-09-2022",
          },
        },
        {
          id: 12,
          name: "Carolyn Thompson",
          photo: "",
          licenceNo: "CTP-3335432",
          vehicle: {},
        },
        {
          id: 13,
          name: "Barbara Wood",
          photo: "https://randomuser.me/api/portraits/women/13.jpg",
          licenceNo: "BW-3333876",
        },
        {
          id: 14,
          name: "David Anderson",
          photo: "https://randomuser.me/api/portraits/men/14.jpg",
          licenceNo: "DA-24465557",
        },
        {
          id: 15,
          name: "Nicole Clarke",
          photo: "https://randomuser.me/api/portraits/women/15.jpg",
          licenceNo: "NC-1009554",
        },
        {
          id: 16,
          name: "Brenda Wilson",
          photo: "https://randomuser.me/api/portraits/women/16.jpg",
          licenceNo: "BW-3224234",
          vehicle: {
            registation: "TJ71NGT",
            make: "VW",
            model: "Golf",
            dateLastDriven: "09-09-2022",
          },
        },
        {
          id: 17,
          name: "Kenneth Phillips",
          photo: "",
          licenceNo: "KP-111765",
        },
        {
          id: 18,
          name: "Michelle Hill",
          photo: "https://randomuser.me/api/portraits/women/18.jpg",
          licenceNo: "MH-2227756",
        },
      ],
    };
  },
  mounted() {
    this.loadedDrivers = true;
  },
};
</script>

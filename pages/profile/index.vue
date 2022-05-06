<template>
  <div class="profile">
    <div class="profile__wrapper">
      <h2>List of Administrators</h2>
      <div class="profile__list">
        <div class="profile__headers">
          <span v-for="(header, idx) in headers" :key="idx">
            {{ header.title }}
          </span>
        </div>
        <div class="profile__list">
          <administrators
            @deleteUser="deleteUser"
            v-for="(item, idx) in administrators"
            :key="idx"
            :administrators="administrators"
            :item="item"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Administrators from "../../components/Administrators.vue";
export default {
  components: { Administrators },
  data() {
    return {
      headers: [
        {
          title: "First Name",
        },
        {
          title: "Second Name",
        },
        {
          title: "Phone",
        },
        {
          title: "Address",
        },
        {
          title: "E-Mail",
        },
      ],
      administrators: [
        {
          first_name: "Yerassyl",
          second_name: "Yeltayev",
          phone_number: "777-99-00",
          address: "Manasa, 34",
          email: "loxich@gmail.com",
        },
        {
          first_name: "Victoriya",
          second_name: "Tolshina",
          phone_number: "777-90-00",
          address: "Manasa, 33",
          email: "vi@gmail.com",
        },
        {
          first_name: "Yerassyl",
          second_name: "Kenzhetay",
          phone_number: "777-99-01",
          address: "Manasa, 32",
          email: "kenzh@gmail.com",
        },
        {
          first_name: "Yan",
          second_name: "Eirikh",
          phone_number: "777-99-02",
          address: "Manasa, 35",
          email: "yan@gmail.com",
        },
        {
          first_name: "Ilyar",
          second_name: "Nazarov",
          phone_number: "777-99-11",
          address: "Manasa, 34",
          email: "ilyar@gmail.com",
        },
        {
          first_name: "Marzhan",
          second_name: "Izteleu",
          phone_number: "777-99-22",
          address: "Manasa, 33",
          email: "morzh@gmail.com",
        },
        {
          first_name: "Zhaparkhanov",
          second_name: "Olzhas",
          phone_number: "777-99-33",
          address: "Manasa, 35",
          email: "osha@gmail.com",
        },
      ],
    };
  },
  methods: {
    deleteUser(id) {
      this.administrators.splice(id, 1);
    },
  },
};
</script>

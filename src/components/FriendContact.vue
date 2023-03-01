<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails()">
      {{ detailsAreVisible ? "Hide" : "Show" }} Details
    </button>
    <ul v-if="detailsAreVisible">
      <li>Phone: {{ friend.phone }}</li>
      <li>Email: {{ friend.email }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  // props: ["name", "phoneNumber", "emailAddress"],
  props: {
    name: {
      type: String,
      required: true,
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    emailAddress: {
      type: String,
      required: true,
    },
    isFavorite: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: this.name,
        name: this.name,
        phone: this.phoneNumber,
        email: this.emailAddress,
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>

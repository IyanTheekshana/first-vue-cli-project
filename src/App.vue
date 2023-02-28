<template>
  <h2>My Friends</h2>
  <ul>
    <li></li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      friends: [
        {
          id: "manuel",
          name: "Manuel Lorenzo",
          phone: "01234567891",
          email: "manuel@localhost.it",
        },
        {
          id: "john",
          name: "John Cena",
          phone: "01234567891",
          email: "john@localhost.it",
        },
      ],
    };
  },
};
</script>

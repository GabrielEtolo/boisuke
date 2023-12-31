<template>
  <nav>
    <ul>
      <li><NuxtLink to="/about">About</NuxtLink></li>
      <li><NuxtLink to="/product">Product</NuxtLink></li>
      <li><NuxtLink to="/contact">Contact</NuxtLink></li>
    </ul>
  </nav>
</template>

<script>
export default {
  // No specific logic for navigation component
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');
nav {
  text-align: center; /* Centering the navigation links */
  font-family: 'Roboto', sans-serif;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  display: inline-block; /* Display links in a line */
  margin-right: 20px; /* Adjust spacing between links */
}

li:last-child {
  margin-right: 0; /* No margin for the last item */
}

a {
  text-decoration: none;
  color: black; /* Text color for links */
  font-size: 16px; /* Adjust the size as needed */
  font-weight: bold; /* Make the font bold */
}

/* Add styles for a hover effect */
a:hover {
  color: #f00; /* Change color on hover */
  transition: color 0.3s ease; /* Smooth transition for hover effect */
}
</style>

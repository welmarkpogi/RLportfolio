<template>
  <div class="container">
    <div class="profile-wrapper">
      <img src="@/assets/rl.jpg" alt="Profile Image" class="profile-image">
    </div>
    <strong>
      <p class="blue-text">Authenticity is my paintbrush. It's about embracing myself fully, 
        <br>Cherishing genuine connections, and celebrating the unique beauty of my identity.
      </p>
    </strong>
  </div>
</template>

<style scoped>
.container {
  background: linear-gradient(to bottom, #17e064, #35d309); 
  background-size: cover; 
  background-repeat: no-repeat; 
  background-position: center; 
  height: 100vh; /* Full height of viewport */
  width: 100vw; /* Full width of viewport */
  padding: 100px 0; /* Adjust vertical padding */
  border-radius: 10px;
  color: #333; 
  background-color: rgba(255, 255, 255, 0.7);
  display: flex; /* Use flexbox */
  flex-direction: column; /* Arrange items vertically */
  justify-content: center; 
  align-items: center; 
}

.profile-wrapper {
  text-align: center; /* Align the text to the center */
}

.profile-image {
  width: 150px; /* Adjust image width as needed */
  height: 150px; /* Adjust image height as needed */
  border-radius: 50%; /* Make image round */
  margin-bottom: 20px; /* Add margin below image */
}

.blue-text {
  color: black; 
}
</style>

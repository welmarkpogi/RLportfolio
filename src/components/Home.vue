<template>
  <div id="home" class="striped-bg">
    <div class="container">
      <div class="content">
        <div class="picture"></div>
        <br>
        <strong><h1 class="text">Hello! It's me RL Suarez</h1></strong>
        <div class="text-container">
          <p class="text">A 3rd year BSIT student, my personal life is about love, family, and authenticity.
            <br>It's about embracing who I am, cherishing meaningful connections, 
            <br>and advocating for equality with pride.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#home {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.container {
  text-align: center;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.picture {
  width: 200px;
  height: 200px;
  background-color: rgba(173, 216, 230, 0.7); /* Change background color here */
  background-image: url('@/assets/rl.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  border-radius: 50%;
  margin-bottom: 20px;
}

.text {
  margin: 0;
  color: white; /* Change text color to white */
}

.text-container {
  overflow: hidden;
  white-space: nowrap;
}

.text-container p {
  animation: textScroll 20s linear infinite; /* Adjust the speed and duration of the animation as needed */
}

@keyframes textScroll {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}

/* Rainbow color theme */
.striped-bg {
  background-image: repeating-linear-gradient(45deg, 
    #FF0000,
    #FFD700 30px,
    #008000 30px,
    #008000 60px);
  margin: 0;
  padding: 0;
}
</style>

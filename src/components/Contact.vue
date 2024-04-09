<template>
  <div class="contact-wrapper">
    <div class="contact-container animated fadeIn">
      <div class="card">
        <h4 class="card-header dancing-text">Personal Information</h4>
        <div class="card-body contact-warning">
          <table>
            <tr>
              <td><strong>Name:</strong></td>
              <td>RL Suarez</td>
            </tr>
            <tr>
              <td><strong>Gender:</strong></td>
              <td>Female</td>
            </tr>
            <tr>
              <td><strong>Birthdate:</strong></td>
              <td>June 25, 2000</td>
            </tr>
            <tr>
              <td><strong>Age:</strong></td>
              <td>23</td>
            </tr>
            <tr>
              <td><strong>Address:</strong></td>
              <td>Gabi Cordova Cebu</td>
            </tr>
            <tr>
              <td><strong>School:</strong></td>
              <td>Cordova Public College</td>
            </tr>
            <tr>
              <td><strong>Course:</strong></td>
              <td>College of Information Technology</td>
            </tr>
            <tr>
              <td><strong>Email Address:</strong></td>
              <td>runelynbinuloac@gmail.com</td>
            </tr>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contact-wrapper {
  background: linear-gradient(to bottom, #17e064, #35d309); /* Static linear gradient background */
}

.contact-container {
  margin: 10%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  border-radius: 10px;
  color: #333;
}

.card {
  width: 100%;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.card-header {
  background-color: #38db1e;
  color: #fff;
  padding: 10px;
  border-radius: 10px 10px 0 0;
}

.card-body {
  padding: 20px;
}

/* Dancing text animation */
.dancing-text {
  animation: dance 2s ease infinite;
  color: aquamarine; /* Change text color to aquamarine */
}

@keyframes dance {
  0%, 100% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(10px);
  }
}

/* Animation */
.animated {
  animation-duration: 10s;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Table styles */
table {
  width: 100%;
}

table td {
  padding: 10px;
  border-bottom: 1px solid #310c0c;
}

table tr:last-child td {
  border-bottom: none;
}
</style>

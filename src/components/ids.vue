<template>
  <div class="ids-dashboard">
    <h2 class="ids-heading">Intrusion Alerts</h2>
    <div class="ids-alerts">
      <div v-if="alerts.length === 0" class="no-alerts">No intrusion alerts found.</div>
      <div v-else>
        <div v-for="alert in filteredAlerts" :key="alert._id" class="ids-alert">
          <div class="alert-header">
            <h3 class="alert-title">{{ alert.SSID }} Alert</h3>
            <button class="fix-alert" @click="fixAlert(alert)">Fix Alert</button>
          </div>
          <div class="alert-details">
            <p><strong>Alert ID:</strong> {{ alert._id }}</p>
            <p><strong>MAC Address:</strong> {{ alert.MACAddress }}</p>
            <p><strong>Signal Strength:</strong> {{ alert.signalStrength }} dBm</p>
            <p><strong>Encryption Type:</strong> {{ alert.encryptionType }}</p>
            <p><strong>Channel:</strong> {{ alert.channel }}</p>
            <p><strong>IP Address:</strong> {{ alert.ipAddress }}</p>
            <p><strong>Subnet Mask:</strong> {{ alert.subnetMask }}</p>
            <p><strong>Alert Time:</strong> {{ formatTimestamp(alert.createdAt) }}</p>
            <p v-if="alert.isFixed" class="alert-fixed">Alert has been fixed!</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, computed } from 'vue'

const alerts = ref([])

// Fetch intrusion alerts data from the API
async function fetchIntrusionAlertsData() {
  try {
    const response = await fetch('https://uml-api.vercel.app/api/intrusionAlerts')
    const data = await response.json()
    alerts.value = data
  } catch (error) {
    console.error('Error fetching intrusion alerts data:', error)
  }
}

onMounted(() => {
  fetchIntrusionAlertsData()
})

// Function to fix an intrusion alert
function fixAlert(alert) {
  // For demo purposes, let's simulate a delay of 2 seconds to fix the alert.
  // Replace this logic with actual IDS fixing process in a real application.
  console.log('Fixing alert:', alert._id)
  alert.isFixed = true // Marking the alert as fixed
  setTimeout(() => {
    alert.isFixed = false // Resetting the fixed status after 2 seconds (for demo purposes)
  }, 2000)
}

// Function to format the timestamp
function formatTimestamp(timestamp) {
  const date = new Date(timestamp)
  return date.toLocaleString()
}

// Computed property to filter alerts based on search query
const searchQuery = ref('')

const filteredAlerts = computed(() => {
  return alerts.value.filter(alert =>
    alert.SSID.toLowerCase().includes(searchQuery.value.toLowerCase())
  )
})
</script>


<style scoped>
/* Add your CSS styling for the IDS dashboard here */
.ids-dashboard {
  background-color: #000000;
  color: #ffffff;
  padding: 20px;
}

.ids-heading {
  font-size: 32px;
  margin-bottom: 20px;
}

.ids-alerts {
  display: grid;
  grid-gap: 20px;
}

.no-alerts {
  padding: 10px;
  border-radius: 4px;
  background-color: #303030;
}

.ids-alert {
  padding: 20px;
  border-radius: 4px;
  background-color: #303030;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.alert-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.alert-title {
  margin: 0;
  font-size: 24px;
}

.fix-alert {
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  background-color: #007bff;
  color: #ffffff;
  cursor: pointer;
}

.alert-details {
  margin-top: 10px;
  color: #cccccc;
}

.alert-details p {
  margin: 5px 0;
}

/* Add styles for the fixed alerts */
.alert-item-fixed {
  background-color: #008000; /* Green background for fixed alerts */
}
</style>

<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Footer from './components/Footer.vue'
import Modal from './components/Modal.vue'
import Appointments from './components/Appointments.vue'

export default {
  components: {
    Navbar,
    Home,
    Footer,
    Modal,
    Appointments
  },
  data() {
    return {
      currentPage: 'Home',
      modal: false,
      appointment: [],
    }
  },
  methods: {
    receivedPage(page) {
      this.currentPage = page;
    },
    openModal(mod) {
      this.modal = mod;
    },
    closeModal(mod) {
      this.modal = mod;
    },
    receiveForm(fullname, age, address, date, petType, color, dogAge, breed, petSickness) {
      this.appointment.push({ ...fullname, age, address, date, petType, color, dogAge, breed, petSickness })
    }
  },

}
</script>

<template>
  <Navbar @goTo="receivedPage" @openModal="openModal" />
  <Home v-if="currentPage === 'Home'" />
  <Appointments v-if="currentPage === 'Appointments'" :sendForm="this.appointment" />
  <Modal v-if="modal === true" @closeModal="closeModal" @send-to="receiveForm" />
  <Footer />

</template>

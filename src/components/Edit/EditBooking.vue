<template>
  <div>
    <form @submit.prevent="handleUpdateForm">
      <div>
        <input
          type="text"
          class="form-control form-control-sm mt-3"
          placeholder="Name"
          v-model="guest.name"
          required
        />
        <input
          type="email"
          class="form-control form-control-sm mt-3"
          placeholder="Email Address"
          v-model="guest.email"
          required
        />
        <input
          type="text"
          class="form-control form-control-sm mt-3"
          placeholder="Phone Number"
          v-model="guest.phone"
          required
        />
        <input
          type="text"
          class="form-control form-control-sm mt-3"
          placeholder="Number of Guests"
          v-model="guest.guestNum"
          required
        />
        <br />
        <p>Accommodation and Visitation Date:</p>
        <input
          class="btn-radio"
          type="radio"
          value="Container House"
          v-model="guest.accommodationType"
        />
        <label>Container House</label>
        <br />
        <input
          class="btn-radio"
          type="radio"
          value="Camping Tent"
          v-model="guest.accommodationType"
        />
        <label>Camping Tent</label>
        <br />
        <input
          class="btn-radio"
          type="radio"
          value="Cottage"
          v-model="guest.accommodationType"
        />
        <label>Cottage</label>
        <br />
        <input
          type="date"
          class="form-control form-control-sm mt-3"
          v-model="guest.checkin"
          required
        />
        <input
          type="date"
          class="form-control form-control-sm mt-3"
          v-model="guest.checkout"
          required
        />
        <br />
        <input
          class="btn btn-success btn-block"
          type="submit"
          value="Update Booking"
        />
      </div>
    </form>
    <em>{{ message }}</em>
    <br />
  </div>
</template>

<script>
import axios from 'axios';
import api from '../../api';

export default {
  props: {
    message: String,
  },
  data() {
    return {
      guest: {},
    };
  },
  // edit-button onClick GETs this guest.
  created() {
    axios.get(`${api}/guest/${this.$route.params.id}`).then((res) => {
      this.guest = res.data;
    });
  },
  //
  methods: {
    async handleUpdateForm() {
      // update-button onClick, POSTs this guest.
      try {
        await axios.post(`${api}/update-guest/${this.$route.params.id}`, this.guest).then(() => {
          this.$router.push('/admin');
        });
        this.message = 'Sent Successfully';
      } catch {
        this.message = 'Unsuccessful! Please, Try Again.';
      }
    },
  },
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}

h5 {
  color: #068d68;
}

p {
  font-size: 10pt;
  text-align: center;
}

form {
  text-align: left;
  font-size: 10pt;
}

.btn-radio {
  margin-right: 10px;
}

em {
  color: red;
  font-size: 10pt;
  text-align: center;
}
</style>

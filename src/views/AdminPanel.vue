<script setup>
import EmployeeList from "../components/AdminPanel/EmployeeList.vue";
import GuestList from "../components/AdminPanel/GuestList.vue";
import ActivityList from "../components/AdminPanel/ActivityList.vue";
import AccommodationList from "../components/AdminPanel/AccommodationList.vue";
</script>

<template>
  <div class="wrapper">
    <br />
    <ul
      class="nav nav-tabs mb-3 justify-content-center"
      id="pills-tab"
      role="tablist"
    >
      <li class="nav-item" role="presentation">
        <button
          class="nav-link active"
          id="pills-employees-tab"
          data-toggle="pill"
          data-target="#pills-employees"
          type="button"
          role="tab"
          aria-controls="pills-employees"
          aria-selected="true"
        >
          Employees
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button
          class="nav-link"
          id="pills-guests-tab"
          data-toggle="pill"
          data-target="#pills-guests"
          type="button"
          role="tab"
          aria-controls="pills-guests"
          aria-selected="false"
        >
          Guests
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button
          class="nav-link"
          id="pills-activities-tab"
          data-toggle="pill"
          data-target="#pills-activities"
          type="button"
          role="tab"
          aria-controls="pills-activities"
          aria-selected="false"
        >
          Activities
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button
          class="nav-link"
          id="pills-accommodations-tab"
          data-toggle="pill"
          data-target="#pills-accommodations"
          type="button"
          role="tab"
          aria-controls="pills-accommodations"
          aria-selected="false"
        >
          Accommodations
        </button>
      </li>
    </ul>
    <div id="greetings-container">
      <p>
        Good {{ setGreeting }} {{ claims.name }}<br /><RouterLink
          style="margin-left: 10px"
          to="/forms/new"
          ><input type="button" class="btn btn-outline-info" value="add record"
        /></RouterLink>
        <!-- Logout -->
        <button class="btn btn-danger" @click="logout()">Logout</button>
      </p>
    </div>

    <div class="tab-content" id="pills-tabContent">
      <div
        class="tab-pane fade show active"
        id="pills-employees"
        role="tabpanel"
        aria-labelledby="pills-employees-tab"
      >
        <EmployeeList />
      </div>
      <div
        class="tab-pane fade"
        id="pills-guests"
        role="tabpanel"
        aria-labelledby="pills-guests-tab"
      >
        <GuestList />
      </div>
      <div
        class="tab-pane fade"
        id="pills-activities"
        role="tabpanel"
        aria-labelledby="pills-activities-tab"
      >
        <ActivityList />
      </div>
      <div
        class="tab-pane fade"
        id="pills-accommodations"
        role="tabpanel"
        aria-labelledby="pills-accommodations-tab"
      >
        <AccommodationList />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hours: new Date().getHours(),
      claims: "",
      authenticated: false,
    };
  },
  computed: {
    setGreeting() {
      if (this.hours >= 0 && this.hours < 12) {
        return "Morning";
      }
      if (this.hours >= 12 && this.hours < 17) {
        return "Afternoon";
      }
      return "Evening";
    },
  },
  async created() {
    await this.isAuthenticated();
    this.$auth.authStateManager.subscribe(this.isAuthenticated);
    // OKTA CLAIMS
    this.setup();
  },
  watch: {
    // Everytime the route changes, check for auth status
    $route: "isAuthenticated",
  },
  methods: {
    // OKTA CLAIMS
    async setup() {
      this.claims = await this.$auth.getUser();
    },
    async isAuthenticated() {
      this.authenticated = await this.$auth.isAuthenticated();
    },
    async logout() {
      await this.$auth.signOut();
    },
  },
};
</script>

<template>
  <br />
  <div>
    <div class="card-data">
      <div
        v-for="employee in employeeList"
        :key="employee._id"
        class="employee-data"
      >
        <div class="card">
          <img
            :src="'../../../backend/uploads/' + employee.fileName + '.jpg'"
            alt="employee"
          />
          <div class="card-body">
            <p>
              {{ employee.fileName }}<br />{{ employee.role }}<br />{{
                employee.description
              }}
            </p>
            <!-- CONTROLS -->
            <p>
              <!-- EDIT RECORD -->
              <RouterLink
                :to="{ name: 'edit-profile', params: { id: employee._id } }"
              >
                <input
                  style="border: none"
                  type="button"
                  class="btn-outline-info"
                  value="edit"
                />
              </RouterLink>

              <!-- DELETE RECORD -->
              <RouterLink to="" @click.prevent="removeEmployee(employee._id)">
                <input
                  style="border: none"
                  type="submit"
                  class="btn-outline-danger"
                  value="delete"
                />
              </RouterLink>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { useEmployeeStore } from "../../stores/EmployeeStore";
import { mapStores, mapState, mapActions } from "pinia";
export default {
  computed: {
    // State and Getters
    // other computed properties
    ...mapStores(useEmployeeStore),
    ...mapState(useEmployeeStore, ["employeeList", "employeeCount"]),
  },
  created() {
    this.getEmployee();
  },
  methods: {
    // Actions
    ...mapActions(useEmployeeStore, ["getEmployee", "removeEmployee"]),
  },
};
</script>

<template>

  <div class="content">
    <div>
      <h3>Select domain</h3>
      <multiple-select title='Years'/>
      <multiple-select title='Domains'/>
       <h3>Select year</h3>
    </div>
    <div class="md-layout">
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100"      >
        <md-card>
          <md-card-header data-background-color="green">
            <h4 class="title">Companies visited in year  </h4>
            <p class="category">Here is a subtitle for this table</p>
          </md-card-header>
          <md-card-content>
            <simple-table table-header-color="purple"></simple-table>
          </md-card-content>
        </md-card>
      </div>

      <!-- <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100">
        <md-card class="md-card-plain">
          <md-card-header data-background-color="green">
            <h4 class="title">Table on Plain Background</h4>
            <p class="category">Here is a subtitle for this table</p>
          </md-card-header>
          <md-card-content>
            <ordered-table></ordered-table>
          </md-card-content>
        </md-card>
      </div> -->
    </div>
    
  </div>
  
</template>

<script>
import { SimpleTable } from "@/components";
import MultipleSelect from "../components/MulipleDropdown.vue"
export default {
  components: {
    // OrderedTable,
    SimpleTable,
    MultipleSelect
    // Dropdown
},
};
</script>

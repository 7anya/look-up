<template>
  <div>
    
    <md-table v-model="users" :table-header-color="tableHeaderColor">
    
      <md-table-row v-if="true || item.years.includes('2019') && item.domain.includes('finance')" slot="md-table-row" slot-scope="{item}">
        <md-table-cell md-label="Company name">
          <div >
            {{ item.companyName }}
            <DialogueCustom title="hello"/>
          </div></md-table-cell>
        <md-table-cell md-label="Domain"><div :key="item" v-for="item of item.domain">{{ item }}, </div></md-table-cell>
        <md-table-cell md-label="City">{{ item.city }}</md-table-cell>
        <md-table-cell md-label="Salary">{{ item.salary }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
import DialogueCustom from "../ShowDescription.vue"
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: "",
    },
  },
  components: {DialogueCustom},
  data() {
    return {
      selected: [],
      users: [
        {
          companyName: "Dundar milflin paper company",
          salary: "$36,738",
          domain: ["finance, analytics"],
          city: "Oud-Turnhout",
          years: ["2020",'2019',"2017","2016"],
          jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },
            {
          companyName: "Olivandar's wand shop",
          salary: "$36,738",
          domain: ["Analytics"],
          city: "Oud-Turnhout",
          years: ["2020","2018","2017","2015"],
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },
               {
          companyName: "Gringotts",
          salary: "$36,738",
          domain: ["Analytics", "finance"],
          city: "Diagon ALley",
          years: ["2020","2019","2017","2016"],
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },
               {
          companyName: "Top Gun Academy",
          salary: "$36,738",
          domain: ["Flying"],
          city: "flying",
           years: ["2020","2018","2017","2016"],
            jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },
               {
          companyName: "Jacob's Bakery",
          salary: "$36,738",
          domain: ["culinary"],
          city: "Oud-Turnhout", 
           years: ["2020","2018","2017","2016"], 
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],


        },
               {
          companyName: "Zara",
          salary: "$36,738",
          domain: ["Analytics", "finance"],
          city: "Oud-Turnhout",
          years: ["2020","2018","2017","2016"],
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },
               {
          companyName: "McDonalds",
          salary: "$36,738",
          domain: "Niger",
          city: "Oud-Turnhout",
          years: ["2020","2018","2017","2016"],
           jobDescription:"abcdfrcd",
          questionsAsked: ["abc","abc","abc","osdues"],

        },]
    };
  },
};
</script>

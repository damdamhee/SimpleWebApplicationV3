<template>
  <div>
    <j-header></j-header>
    <j-button v-on:input="addNewPerson"></j-button>
    <j-divider></j-divider>
    <j-table :headers="headers" :values="values"></j-table>
  </div>
</template>
<script>
import JHeader from "@/JHeader.vue";
import JButton from "@/JButton.vue";
import JDivider from "@/JDivider.vue";
import JTable from "@/JTable.vue";
export default {
  name: "App",
  components: { JHeader, JButton, JTable, JDivider },
  data() {
    return {
      headers: ["Name", "Phone No.", "Address"],
      values: [
        { name: "JJH", phno: "010-1234-5678", addr: "suwon" },
        { name: "JHJ", phno: "010-0987-6543", addr: "suwon" }
      ]
    };
  },
  methods: {
      addNewPerson:function(){
          let newPerson = {name:"", phno:"", addr:""}
          this.values.push(newPerson);
      }
  }
};
</script>

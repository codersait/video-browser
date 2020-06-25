<template>
  <div>
    <div class="search-input d-flex">

    <input @keypress.enter="onInput" placeholder="Search" /> 
    <!-- <span @click="search"><i class="fas fa-search"></i></span> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  methods: {
    onInput: function(event) {
      this.$emit("termChange", event.target.value);
    },
    
  }
};
</script>

<style scoped>
span{
  display: inline-block;
  width: 65px;
  background-color: #f8f8f8;
  border: 1px solid #ddd;
}
span:hover{
  background-color: rgb(233, 231, 231);
  color:red
}
i{
  color:rgb(94, 94, 94)
}

div{
  text-align: center;
  margin: 20px;}
div input{
  padding: 1px 7px;
  width: 75%;
  border: 1px solid #ddd;
}
</style>
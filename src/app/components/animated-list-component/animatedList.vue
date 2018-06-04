<template src="./animatedList.html"></template>
<style src="./animatedList.scss" scoped lang="scss"></style>

<script>
  import {httpWrapper} from "../../http/http-wrapper";
  import todoItem from "./todo-item/todoItem";


  export default {
    data(){
      return{
        people:[],
        currentPage: 1,
        loadingData: false,
        animating: false
      }
    },
    components:{
      'todo-item': todoItem
    },
    created(){
      this.getPeopleFromServer();
      this.loadingData = false;

    },
    methods: {
      getPeopleFromServer(){
        httpWrapper.getPeople(this.currentPage,(peopleFromServer) => {
          this.people = peopleFromServer;
        });
      }
    },
    computed: {

    }
  }
</script>


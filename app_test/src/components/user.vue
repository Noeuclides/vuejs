<template lang="html">
 <div class="users">
   <h1>HI USER</h1>
   <ul>
     <li v-for="u in user">
        {{u.name}} - {{u.email}}
     </li>
   </ul>
   <form v-on:submit.prevent="addUser">
     <input type="text" v-model="newUser.name" placeholder="Name">
     <input type="email" v-model="newUser.email" placeholder="email">
     <button type="submit">
       ADD
     </button>
   </form>
 </div>

</template>

<script>
export default {
  data() {
    return {
      user: [
        {
          name: "Joe",
          email: "ada@mail.com",
          contacted: false
        },
        {
          name: "Jhon",
          email: "jhon@mail.com",
          contacted: false
        },
        {
          name: "AlJoe",
          email: "Alada@mail.com",
          contacted: true
        }
      ],
      newUser: {}
    }
    },
    methods: {
      addUser(e) {
        console.log('agregando Usuario');
      }
    }
}
</script>

<style lang="css">
  .users {
     background: #333;
     color: #fff;
     padding: 20px;
  }
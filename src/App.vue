
<template>
   <h1>GitHub Profiles</h1>
   <div class="container-card">
    <base-gird-card v-for="{id,name} in usernames" :username="name" :key="id"></base-gird-card>
   </div>
    <notification-message header="you are welcome" type="error">
    You are my sunshine!
   </notification-message> 
   <notification-message >
    let's me told you some thing, that is really important today . 
    You're bold, you are brilant and beautiful. There are not other people like you 
   </notification-message> 
</template>
<script>
import BaseGirdCard from './components/BaseGirdCard.vue';
import NotificationMessage from "./components/NotificationMessage.vue"
export default{
  components:{'base-gird-card':BaseGirdCard,'notification-message': NotificationMessage},
  data() {
    return {
      usernames:[
        {
          id: 1,
          name:'danielkellyio',
        },
        {
          id: 2,
          name:'defunkt',
        },
        {
          id: 3,
          name:'pjhyett',
        },
        {
          id: 4,
          name:'ezmobius',
        },
        {
          id: 5,
          name:'ivey',
        }
      ]
    }
  },
}

</script>
<style>
body {
  background: #eff8ff;
  height: 100vh;
  width: 100vw;
  font-family: system-ui, BlinkMacSystemFont, -apple-system, Segoe UI, Roboto,
    Oxygen, Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  padding: 0;
  margin-top: 200px;
}

.counter {
  font-size: 0.8rem;
  padding-left: 10px;
  padding-right: 10px;
}

#app {
  background: #fff;
  padding: 2rem;
  margin: 1rem;
  border-radius: 3px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.12), 0 2px 4px 0 rgba(0, 0, 0, 0.08);
  width: 95%;
  max-width: 900px;
}

h1 {
  color: #3d4852;
}

ul {
  list-style: none;
  padding: 0;
}

a {
  color: #6cb2eb;
  font-size: 1.25rem;
  transition: all 0.1s ease-in;
  margin-top: 0.5rem;
  display: block;
}

a:hover {
  color: #3490dc;
}

.container-card{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}
.container-card > div{
  flex-basis: 24%;
}
</style>
<template>
  <!--<div>
    <div v-if="!repoUrl">loading...</div>
    <div v-else>most star repo is <a :href="repoUrl">{{repoName}}</a></div>
  </div>-->

  <div class="container">
    <Search/>
    <UsersMain/>
  </div>
</template>

<script>
  import axios from 'axios'
  import Search from './components/Search'
  import Main from './components/Main'

  export default {
    components: {
      Search,
      UsersMain: Main
    }


    /*data() {
      return {
        repoUrl: '',
        repoName: ''
      }
    },
    mounted() { //初始化的时候
      //发送ajax请求数据
      const url = 'https://api.github.com/search/repositories?q=vue&sort=stars'
      /!*this.$http.get(url).then(
        response => {
          const result = response.data
          const mostRepo =result.items[0]
          this.repoUrl = mostRepo.html_url
          this.repoName = mostRepo.name
        },
        response => {
          console.log("error")
        }
      )*!/

      //使用axios发送ajax请求
      axios.get(url).then(
        response => {
          const result = response.data
          const mostRepo =result.items[0]
          this.repoUrl = mostRepo.html_url
          this.repoName = mostRepo.name
        }
      ).catch(error=>{
        alert("error")
      })
    }*/
  }
</script>

<style>

</style>

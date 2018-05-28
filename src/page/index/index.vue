<template>
  <div>
    <Header></Header>
    <div class="article_list">
      <ul>
         <!--<li v-for="item in list">
          <time v-text="item.create_at"></time>
          <router-link :to="'/content/' + item.id">
            {{ item.title }}
          </router-link>
        </li>-->
      </ul>
    </div>
    <Footer></Footer>
  </div>
</template>
<script>
import Header from '../../components/header.vue'
import Footer from '../../components/footer.vue'
export default {
  // created () {
  //   this.$api.get('topics', null, res => {
  //     console.log(res)
  //   })
  // }
 　components: { Header, Footer },
  data () {
    return {
      list: []
    }
  },
  created () {
    this.getData()
  },
  methods: {
    getData () {
      this.$api.get('health_bases/get_base_list?session_3rd=23ce831e0fb28850de8f70950e707def83d7b19c', null,res => {
            console.log(res.error)
            this.list = res.data
         })
    }
  }
}
</script>
<style>
  .article_list {margin: auto;}
</style>
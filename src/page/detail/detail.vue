<template>
  <div>
    <Header></Header>
    <h2 v-text="article.title"></h2>
    <p>作者：　　发表于：{{article.create_at}}</p>
    <hr>
    <article v-html="article.content"></article>
    <h3>网友回复：</h3>
    <ul>
      <li v-for="item in article.replies">
        <p>评论者：{{item.author.loginname}}　　评论于：{{item.create_at}}</p>
        <article v-html="item.content"></article>
      </li>
    </ul>
    <Footer></Footer>
  </div>
</template>
<script>
	import Header from '../../components/header.vue'
	import Footer from '../../components/footer.vue'
	//console.log(this.$route)
	export default {
	  // created () {
	  //   this.$api.get('topics', null, res => {
	  //     console.log(res)
	  //   })
	  // }

	 　components: { Header, Footer },
	  data () {
	    return {
	      id:this.$route.params.id,
	      article: {}
	    }

	  },
	  created () {
	    this.getData()
	    //console.log(this.$route.params.id)
	  },
	  methods: {
	    getData () {
	      this.$api.get('topic/' + this.id, null, res => {
	      	 console.log(res)
	      	 this.article = res.data
          })
	    }
	  }
	}
</script>

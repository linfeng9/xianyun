<template>
  <div>
    <Header/>
    <nuxt />
    <Footer/>
  </div>
</template>
<script>
import Header from "@/components/header"
import Footer from "@/components/footer"
export default {
  components:{
    Header,
    Footer
  }
}
</script>

<style>
*{
  margin: 0;
  padding:0
}
ol,li{
  list-style: none
}
a{
  color:inherit;
  /* 使a标签能继承父级的颜色  */
  text-decoration: none
  /* 对文本的修饰 */
}
em,i{
  font-style: normal;
  /* 取消斜体 */
}
</style>

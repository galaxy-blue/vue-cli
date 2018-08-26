<template>
  <div>
    这是demo组件
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },
  mounted () {
    this.bus.$on('changearr',(res)=>{
      console.log(res);
    })

  },
  methods: {

  }

}
</script>

<style>

</style>

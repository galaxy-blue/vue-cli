<template>
 <div class="bg">
   <div class="inputBox">
     <div class="title">{{title}}</div>
     <div class="butto">
     <div class="foot">
         <input type="text" v-model="user" name="username" value="" placeholder="请输入您的用户名" class="textBox ">
         <img :src="txtOne" alt="" class="ren">
         <input type="password" v-model="pwd" name="psw" value="" placeholder="请输入密码" maxlength="6" class="textBox ">
         <img :src="txtTwo" alt="" class="sou">
         <input type="submit" name="sbt" value="登 录" class="loginBox" @click="denglu">
     </div>
     </div>
   </div>
 </div>
</template>

<script>
export default {
  data(){
    return{
      user: '',
      pwd :'',
      title:'河北工程大学',
      txtOne:require('../assets/images/ren.png'),
      txtTwo:require('../assets/images/sou.png'),
    }
  },
  methods:{
    denglu(){
      // 发送请求
      // if(this.user ==''|| this.pwd == '' ) {
      //   return false;
      // }
      //ajax
      // this.axios({
      //   methods:'post',
      //   url:'',
      //   params:{
      //     name:this.user,
      //     pass:this.pwd,
      //   }
      // }).then((res)=>{
      //   //写后台返回的东西
      // })
      this.bus.$emit('changearr',[1,2,3,4]);
      this.$router.push('/demo');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.bg{
  position: absolute;
  top: 0;
  bottom: 0;            /* 撑开 */
  background: #ccc;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.inputBox{
  width:610px;
  height: 475px;
  border:6px solid #7d909b;
  border-radius: 5px;
}
.title{
  width: 100%;
  height:92px;
  background: #242b31;
  color:#fff;
  text-align: center;
  line-height: 92px;
  font-size: 28px;
}
.butto{
  width: 100%;
  height: 380px;
  background: #fff;
  padding:1px;
}
.foot{
      width: 411px;
    height: 230px;
    margin: 38px auto;
}
.ren{
position: absolute;
top:180px;
left:490px;
}
.sou{
  position: absolute;
  top:260px;
  left:490px;
}
.textBox {
    width: 415px;
    height: 52px;
    margin-bottom: 23px;
    border: 1px solid #d2dbe2;
    border-radius: 2px;
    padding-left: 58px;
    box-sizing: border-box;
}
.loginBox {
    margin: 33px auto 0;
    margin-left: 84px;
    width: 247px;
    height: 50px;
    background: #04c3b3;
    border: 1px solid #04c3b3;
    border-radius: 5px;
    color: #fff;
    font-size: 23px;
    cursor: pointer;
}
</style>

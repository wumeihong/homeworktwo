<template>
  <div class="guanggao">
        <h1>广告创意</h1>
        <div class="top">
            <h3>落地页</h3>
            <label for="">着陆页地址:<input type="text" placeholder="请设置广告名称"/><span>预览</span></label>
        </div>
        <div class="middle">
            <h3>上传创意</h3>
            <a href="javascript:;" v-on:click="tocreatives" @click="open">+添加创意</a>
        </div>
        <div class="bottom">
            <button>提交</button>
        </div>
  </div>
</template>
<script>
export default {
  name:"guanggao",
  methods:{
      tocreatives(){
          this.$router.push("/creatives")
      },
       open() {
        this.$alert('<strong>单图</strong><strong>多图</strong>', '选择样式', {
          dangerouslyUseHTMLString: true,
          showConfirmButton:false,
          showClose:false,
          center:true

        });
      }
  }
}
</script>
<style lang=less scoped>
    .guanggao{
        width:100%;
        height: 100%;
        padding: -10px -10px;
       h1{
           width: 100%;
           height: 50px;
           line-height: 50px;
           font-size: 28px;
           font-weight: normal;
       }
       .top{
           margin-top:10px;
           h3{
               font-size: 20px;
           }
           label{
               display: block;
               color:#333;
               margin-top:10px;
               font-size: 14px;
               input{
                   margin-left: 5px;
                   border: 1px solid #ddd;
                   border-radius: 5px;
                   width:500px;
                   height: 30px;
                   padding-left: 10px;
               }
               span{
                   margin-left: 5px;
                   color:#333;
               }
           }
       }
       .middle{
            margin-top: 80px;
            h3{
                width:100%;
                height: 50px;
                line-height: 50px;
                font-size: 20px;
            }
            a{
                text-decoration: none;
            }
       }
       .bottom{
           margin-top: 50px;
           button{
               width: 150px;
               height: 50px;
               border: none;
               background: #ccc;
               color: #eee;
               border-radius: 10px;
           }
       }
    }
</style>


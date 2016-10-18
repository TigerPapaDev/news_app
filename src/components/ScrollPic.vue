<template>
   <swiper :list="list" auto loop></swiper>

</template>

<script>
    import Swiper from  'vux/src/components/swiper'
    export default {
        components:{
            Swiper
        },
       created :
       function(){
                   this.$http.get('http://v.juhe.cn/toutiao/index?key=fa36694efa34b501c70ecc376cd6e54f&type=top').then((response) => {
                    const rawData =   response.body.result.data;
                     var result=[];
                    for (let i =0;i<11; i++) {
                        let item = rawData[i];
                       result.push({'url':item.url,'img':item.thumbnail_pic_s,'title':item.title});
                         //this.list.slice(0,5);
                    }
            this.$set('list',result);
          }, (response) => {this.error = response.error_code});
      },

      data(){
        return {
            list: [],
    }
}
}
</script>


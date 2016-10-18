<template>
    <div>
       <tab :line-width="2" active-color="#fc378c">
          <tab-item :selected="currSelected=== item" v-for="item in menuItems" @click="currSelected = item">{{item}}</tab-item>
      </tab>

  </div>

</template>


<script>
  import {Tab,TabItem} from 'vux/src/components/tab'
  export default {
    components: {
       Tab,TabItem
   },
   data(){
    return {
      currSelected: '头条',
      menuItems: ['头条', '社会', '国内', '国际', '娱乐','体育','军事','科技','财经','时尚']
  }
}
}
</script>

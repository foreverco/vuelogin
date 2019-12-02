<template>
    <div class="col-md-8">
        <h3 class="reply">评论回复：</h3>
        <h2 v-show='comments.length===0'>暂无评论，点击左侧添加评论！！！</h2>
        <ul class="list-group">
          <Item v-for="(comment, index) in comments" :index='index' :key="index" :delComment='delComment' :comment='comment'>
          </Item>
        </ul>
      </div>
</template>

<script type='text/ecmascript-6'>
    import Item from './Item.vue'
    export default {
        // 声明接收值:这个属性就会成为组件对象的值
        props:['comments','delComment'], // 只指定属性名
        components:{
            Item
        },
        data(){
            return {
                
            }
        }
    }
</script>

<style>
        .reply {
  margin-top: 0px;
}


</style>

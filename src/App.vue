<template>
    <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <h1>请发表对Vue的评论</h1>
          </div>
        </div>
      </div>
    </header>
    <div class="container">
        <Add :addComment='addComment'></Add>
        <List :comments="comments" :delComment='delComment'></List>
    </div>
  </div>
</template>

<script type='text/ecmascript-6'>
    import Add from './components/Add.vue'
    import List from './components/List.vue'
    export default {
        data(){
            return {
                comments:[// 数据在哪个组件 更新数据的行为就应该定义在哪个组件
                    {
                        name:'BOB',
                        content:'Vue 还不错'
                    },
                    {
                        name:'cater',
                        content:'Vue 简单'
                    },
                    {
                        name:'lwm',
                        content:'Vue soso'
                    }
                ]
            }
        },
        methods:{
            // 添加评论
            addComment (comment){
                this.comments.unshift(comment)
            },
            // 删除指定下标的评论
            delComment (index){
                this.comments.splice(index,1)
            }
        },
        components:{
            Add,
            List
        }
    }
</script>

<style>

</style>

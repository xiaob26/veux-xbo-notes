<template>
   <div class='ui container notes'>
        <h4 class='ui horizontal divider header'>
          <i class= 'paw icon'></i>
            Wangbo Notes 
        </h4>
        <a href="#" class='ui right floated basic violet button' @click="create">添加笔记</a>
        <div class='ui divided items'>
                <note
                v-for="(entity,index) in entities" :key="index"
                :entity='entity'
                ></note>
          <span class='ui small disabled header'
          v-if='!entities.length'
          >
          还没有笔记，请添加你喜欢的笔记吧！
          </span>
        </div>
       
    </div>
</template>

<script>
import Note from './Note'

import {mapGetters,mapActions} from 'vuex'
export default {
    name:'Notes',
    created() {
        this.initial()
    },
    components: {
        Note
    },
    computed: {
        ...mapGetters([
            'entities'
        ])
    },
    methods: {
      ...mapActions([
          'initial',
          'create'
      ])
    }

}
</script>

<style>

</style>
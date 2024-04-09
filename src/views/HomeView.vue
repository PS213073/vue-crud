<!-- <script>
import { ref, reactive } from 'vue'

// const count = ref(0)
// const state = reactive({
//   count: 0
// })

export defa
  components: { PostItem },ult {
  setup() {
   const count = ref(0)

    return {
      count
    }
  }
}
</script> -->

<!-- <template> -->
  <!-- <button @click="state.count++">Number is {{ state.count }}</button> -->
  <!-- <button @click="count++">Number is {{ count }}</button> -->
<!-- </template> -->

<script setup>
import PostItem from "@/components/PostItem.vue";
import MyWrapper from "@/components/MyWrapper.vue";

const posts = [
  {
    id: 1,
    title: 'This is great book',
    body: 'tellus integer feugiat scelerisque varius morbi enim nuncfaucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '06/04/2023',
    is_saved: false
  },
  {
    id: 2,
    title: 'Coding is fun !? ',
    body: 'tellus integer feugiat scelerisque varius morbi enim nuncfaucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '06/04/2023',
    is_saved: false
  },
  {
    id: 3,
    title: 'Vue js vs react',
    body: 'tellus integer feugiat scelerisque varius morbi enim nuncfaucibus a pellentesque sit',
    author: 'Jon Doe',
    created_at: '06/04/2023',
    is_saved: false
  }
]
</script>

<template> 
  <div v-for="(post, index) in posts" :key="index">
    <MyWrapper>
      <template #header> header </template>
    <PostItem :post="post"/> 
  </MyWrapper>    
  </div>
</template>



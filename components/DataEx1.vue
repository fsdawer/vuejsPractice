<script>
import Practice2Child from '../Practice2Child.vue';
export default {
  components: {
    Practice2Child,
  },
  data() {
    return {
      childName: 'Alice',
    };
  },
  methods: {
    handleGreeting(message) {
      console.log(message);
    },
  },
};
</script>
<template>
  <div>
    <Practice2Child :name="childName" @greet="handleGreeting" />
  </div>
</template>



<script>
export default {
  props: {
    name: String,
  },
  emits: ['greet'],
  methods: {
    sendGreeting() {
      this.$emit('greet', `Hello, ${this.name}!`);
    },
  },
};
</script>
<template>
  <div>
    <button @click="sendGreeting">Send Greeting</button>
  </div>
</template>
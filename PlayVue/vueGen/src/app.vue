<template>
  <div class="main container">
    <input type="text" v-model="text" />
    <div class="hello">Hello {{ text }}!</div>
    <div class="" @click='doSomething'>
      {{ message }}
    </div>
    <div class="text-center">
      <dropdown>
        <button type="button" class="btn btn-success" data-toggle="dropdown">
          Welcome
          <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="#">Action</a></li>
          <li><a href="#">Another action</a></li>
          <li><a href="#">Something else here</a></li>
          <li role="separator" class="divider"></li>
          <li><a href="#">Separated link</a></li>
        </ul>
      </dropdown>
    </div>
  </div>
</template>

<script>
  import { dropdown } from 'vue-strap/dist/vue-strap.js'
  export default {
    replace: false,
  	data() {
      return {
        text: 'vue',
        message: 'hi man'
      }
    },
    components: {
      dropdown
    },
    methods:{
      doSomething :function(){
        this.message = 'message changed';
        this.text = 'text changed';
      }
    }
  }
</script>

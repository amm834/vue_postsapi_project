<template>
  <div>
  <Nav></Nav>
    <slot></slot>
  </div>
</template>
<script type="text/javascript" charset="utf-8">
import Nav from './Nav'
  export default{
    name:'Master',
    components:{
      Nav
    }
  }
</script>
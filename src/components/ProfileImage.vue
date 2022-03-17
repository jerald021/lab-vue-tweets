<template>
      <img
      :src="user.image"
      className="profile"
      alt="profile"
    />
</template>

<script>
export default {
  props: { 
    user:{
      image:{
        type: String,
      }, 
    }                       
  },
}
</script>

<style>

</style>
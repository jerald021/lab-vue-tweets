<template>
    <span className="user">
        <span className="name">{{user.name}}</span>
        <span className="handle">{{user.handle}}</span>
    </span>  
</template>

<script>
export default { 
    props:{
        user:{
            name:{
                type: String,
            },
            handle:{
                type: String,
            }
        }
    },       
}
</script>

<style>

</style>
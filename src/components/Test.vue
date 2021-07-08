<template>
    <div>
        test {{age}}
    </div>
</template>
<script>
export default {
    name: "Test",
    props: {
        age:Number,
    },
    mounted(){
        console.log(this)
    }
}


</script>
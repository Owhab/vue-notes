<template>
    
    <h1>Person Name: {{name}} </h1>
    <h2>Age: {{age}} </h2>
    
</template>
<script>
export default {
    props: ["name", "age"]
    
}
</script>
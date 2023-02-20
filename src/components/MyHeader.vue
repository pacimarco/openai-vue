<template>
  <div class="header">
    <img src="../assets/code.jpeg" alt="code" class="header_img">
  </div>
</template>

<script>
export default {
name: 'MyHeader',
}
</script>

<style scoped lang="scss">

.header {
    max-width: 100%;
    height: 200px;
    margin-bottom: 20px;

    .header_img{
        width: 100%;
        height: 200px;
        object-fit: cover;

        
    }
}
</style>
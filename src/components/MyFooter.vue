<template>
  <div class="my-footer">
      <ul>
          <li>OpenAi</li>
          <li>Chat GPT</li>
          <li>Bot</li>
          <li>AI</li>
          <li>API</li>
      </ul>
  </div>
</template>

<script>
export default {
name: 'My-Footer'
}
</script>

<style scoped lang="scss">

.my-footer{
    margin-top:30px;
    border-top: 5px solid yellow;
    width: 100%;
    height: 150px;
    background-color: black;

    li{
        display:inline-block;
        padding: 10px;
    }

    ul{
        padding:30px;
        margin:auto;
    }

}

</style>
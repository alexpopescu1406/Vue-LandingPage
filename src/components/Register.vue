<template>
<div class="backdrop">
    <div class="modal">
        <h2>{{ header }}</h2>
        <p>{{ text }}</p>
    </div>
</div>
</template>  

<script>
export default {
 data () {
  return {
    header: 'Subscribe to our Newsletter',
    text: 'Get the latest news and best offers!',
  }
},

    
}
</script>
<style> 
.modal {
    width: 600px;
    padding: 20px;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
    color: black !important;
    text-align: center;
}
h2 {
    border: none;
    padding: 0; 
}
.backdrop {
    top: 0;
    position: fixed;
    background: black;
    width: 100%;
    height: 100%;   
}
</style>
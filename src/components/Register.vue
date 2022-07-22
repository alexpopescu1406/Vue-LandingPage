<template>
<div class="backdrop" @click.self="closeModal">
    <div class="modal">
        <slot></slot>
        <div class="actions">
            <slot name="links"></slot>
        </div>
    </div>
</div>
</template>  

<script>
export default {
    methods: {
    closeModal() {
            this.$emit('close')
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
    bottom: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.726);
    width: 100%;
    height: 100%;   
    z-index: 9000;
}

.modal .actions {
    text-align: center;
    margin: 30px 0 10px 0;
    color: red;
}

.modal .actions a {
    background-color: #2f80ed;
  border-radius: 10px;
  border-style: none;
  box-shadow: none;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: Inter,-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif;
  font-size: 15px;
  font-weight: 500;
  height: 50px;
  letter-spacing: normal;
  line-height: 1.5;
  outline: none;
  overflow: hidden;
  padding: 14px 30px;
  position: relative;
  text-align: center;
  text-decoration: none;
}
</style>
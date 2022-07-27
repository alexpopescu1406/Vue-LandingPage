<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal">
      <slot></slot>
        <div class="actions">
          <form @submit="handleSubmit">
            <label>Email: </label>
            <input type="email" required v-model="email" placeholder="email" /><br><br>
            <label>Game events </label>
            <input type="checkbox"><br>
            <label>Game patches </label>
            <input type="checkbox"><br>
            <label>Games on sale </label>
            <input type="checkbox"><br><br>
            <button class="submited">Submit</button>
          </form><br>
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
    },
    handleSubmit() {
        alert("Subscribed")
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
    color: rgb(0, 0, 0);
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

.submited {
  appearance: none;
  backface-visibility: hidden;
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
  transform: translate3d(0, 0, 0);
  transition: all .3s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  display: block;
  margin: auto;
  
}

.submited:hover {
  background-color: #1366d6;
  box-shadow: rgba(0, 0, 0, .05) 0 5px 30px, rgba(0, 0, 0, .05) 0 1px 4px;
  opacity: 1;
  transform: translateY(0);
  transition-duration: .35s;
}

.submited:hover:after {
  opacity: .5;
}

.submited:active {
  box-shadow: rgba(0, 0, 0, .1) 0 3px 6px 0, rgba(0, 0, 0, .1) 0 0 10px 0, rgba(0, 0, 0, .1) 0 1px 4px -1px;
  transform: translateY(2px);
  transition-duration: .35s;
}

.submited:active:after {
  opacity: 1;
}

@media (min-width: 100px) {
  .submited {
    padding: 12px 20px;
    width: 110px;
  }
}
</style>
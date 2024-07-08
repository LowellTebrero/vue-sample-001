<template>
    <div class="modal-backdrop z-50 p-5 md:p-10">
    <div class="bg-color rounded-lg p-5 px-2">
      <header class="modal-header px-4 py-2 lg:px-5 lg:py-4 ">
        <slot name="header">
            This is the default body!
        </slot>
        <button
          type="button"
          class="text-red-400"
          @click="close"
        >
        <Icon icon="mingcute:close-fill" width="1.2rem" height="1.2rem" />
        </button>
      </header>

      <section class="modal-body ">
        <slot name="body">
          This is the default body!
        </slot>
        
       </section>  
    </div>
  </div>
</template>

<script setup>

import { Icon } from '@iconify/vue';


const emit = defineEmits(['close']);

function close(){
  emit('close');
}

window.addEventListener('keydown', (event) => {
  if (event.key === 'Escape') {
    close();
  }
});



</script>

<style scoped>
  .modal-backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(22, 22, 22, 0.719);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;

  }

  .modal-header,
  .modal-footer {
    
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .modal-header {
    position: relative;
    border-bottom: 1px solid #3a3a3a;
    justify-content: space-between;
  }

  .modal-footer {
    border-top: 1px solid #eeeeee;
    justify-content: space-between;
  }

  .modal-body {
    position: relative;
    padding: 20px 10px;
  }

  .bg-color {
    background-color: #080808;
  }

</style>
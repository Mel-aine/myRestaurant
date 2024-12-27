<template>
    <div v-if="isOpen" class="fixed inset-0 flex items-center  justify-center bg-black bg-opacity-40 z-50  ">
      <div class="bg-white rounded-lg shadow-lg w-full max-w-4xl p-3 m-3 md:p-8 relative">
        <div class="flex justify-between items-center  pb-4">
          <h2 class="text-lg md:text-3xl font-bold  text-gray-800">
            {{ title }}
          </h2>
          <button @click="close" class="text-gray-500 hover:text-gray-700 text-xl ">
            <span class="[&>svg]:h-6 [&>svg]:w-6 font-extrabold ">
              <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </span>
          </button>
  
        </div>
        <!-- Contenu -->
        <div class="py-6 p-3  shadow-inner sm:shadow-none  overflow-auto overflow-y-auto min-h-96 max-h-[800px] custom-scrollbar ">
          <slot></slot>
  
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  
  const props = defineProps({
    isOpen: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      default: "",
    },
   
  });
  
  const emit = defineEmits(["close"]);
  
  const close = () => {
    emit("close");
  };
  
  </script>
  <style scoped>
 
  </style>
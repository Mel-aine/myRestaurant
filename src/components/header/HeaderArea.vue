<template>
  <header>
    <nav class="bg-white border-gray-200 px-4 lg:px-6 py-2.5 dark:bg-gray-800 sticky top-0 ">
        <div class="flex flex-wrap justify-between ">
            <a href="" class="flex items-center">
                <img src="../../assets/logo.png" class="mr-3 h-6 sm:h-9 border border-orange-500 rounded-full" alt="EatEasily Logo" />
                <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">EatEasily</span>
            </a>
            <div class="flex items-center space-x-2 lg:order-2">
                
                <button @click="isModalOpen = true" class=" text-gray-800 dark:text-white hover:bg-orange-50 focus:ring-4 focus:ring-orange-300 font-medium rounded-lg text-sm px-2 lg:px-3 py-2 lg:py-2.5 space-x-2">
                <svg class="h-6 w-6 text-orange-500 inline-flex"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.121 17.804A13.937 13.937 0 0112 16c2.5 0 4.847.655 6.879 1.804M15 10a3 3 0 11-6 0 3 3 0 016 0zm6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                    </svg>
                <span class="">Log in</span>
                </button>
                    <button class="text-gray-800 dark:text-white hover:bg-orange-50 focus:ring-4 focus:ring-orange-300 font-medium rounded-full text-sm px-1 lg:px-2 py-1 lg:py-2 mr-2"><svg class="h-6 w-6 text-orange-500"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"/>
                        </svg>
                     </button>
                         <button data-collapse-toggle="mobile-menu-2" type="button" class="inline-flex items-center p-2 ml-1 text-sm text-gray-500 rounded-lg lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="mobile-menu-2" aria-expanded="false">
                    <span class="sr-only">Open main menu</span>
                    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
                    <svg class="hidden w-6 h-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                         </button>
            </div>
             <div class="hidden justify-between items-center w-full lg:flex lg:w-auto lg:order-1" id="mobile-menu-2">
                <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
                    <li>
                        <a href="#" class="block py-2 pr-4 pl-3 text-gray-700 rounded bg-orange-100 lg:bg-transparent lg:text-orange-400  hover:text-gray-950 lg:p-0 dark:text-white" aria-current="page">Restaurants</a>
                    </li>
                    <li>
                        <a href="#" class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-orange-400 lg:p-0 dark:text-gray-400 lg:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent dark:border-gray-700">Order Online</a>
                    </li>
                </ul>
            </div>            
        </div>
    </nav>
    <Modal :isOpen="isModalOpen " @close="isModalOpen = false" />
</header>
</template>

<script setup>
 import { ref } from 'vue';
 import Modal from '../modals/Modal.vue';
import router from '../../router';

const currentRoute = router.currentRoute;
const isModalOpen = ref(false);
</script>
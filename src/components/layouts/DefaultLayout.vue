
<template>
    <!-- ===== Page Wrapper Start ===== -->
    <div class="flex h-screen overflow-hidden">
  
      <!-- ===== Content Area Start ===== -->
      <div class="relative flex flex-1 flex-col overflow-y-auto overflow-x-hidden bg-slate-50 scrollbar-hide">
        <!-- ===== Header Start ===== -->
        <HeaderArea />
        <!-- ===== Header End ===== -->
  
        <!-- ===== Main Content Start ===== -->
        <main>
          <div class=" mx-auto max-w-screen">
            <slot></slot>
          </div>
          
        </main>
        <!-- ===== Main Content End ===== -->
  
        <!-- ===== Footer Start ===== -->
         <FooterArea /> 
        <!-- ===== Footer End ===== -->
      </div>
      <!-- ===== Content Area Start ===== -->
      
      <!-- ===== Sidebar Start ===== -->
      <!-- <SidebarArea /> -->
      <!-- ===== Sidebar End ===== -->
      <!-- <Toast :type="'danger'" :message="'toast.message'" /> -->
    </div>
    <!-- ===== Page Wrapper End ===== -->
  </template>

<script setup>
import HeaderArea from '../header/HeaderArea.vue'
import FooterArea from '../footer/FooterArea.vue'

</script>
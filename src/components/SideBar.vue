<script setup>
    import {defineEmits} from 'vue'

    const emits = defineEmits(['selectOption'])
   
    const selectOption = (isColor) => {
        emits("selectOption", isColor)
    }

</script>

<template>
    <VNavigationDrawer
      expand-on-hover
      rail>
      <VList>
        <VListItem
          prepend-avatar="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80" 
           title="Sandra Yew"
            subtitle="Michaelomaleson@gmail.com"
           >  
        </VListItem>
      </VList>
      <VDivider />

      <VList density="compact" nav>
        <v-list-item @clcik="selectOption(true)" prepend-icon="mdi-image" title="Modern Gallery" value="color" style="color:rgb(7, 79, 13);"></v-list-item>
        <v-list-item @click="selectOption(false)" prepend-icon="mdi-camera" title="Vintage Gallery" value="vintage"></v-list-item>
      </VList>
    </VNavigationDrawer>
</template>
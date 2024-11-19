<template>
    <div>
      <div class="flex flex-col-reverse md:grid md:grid-cols-12 gap-4">
        <Box class="md:col-span-7 flex items-center">
          <div class="w-full">
            <div class="flex items-center gap-2">
              <Price :price="listing.price" class="text-2xl font-bold" />
            </div>
            <ListingSpace :listing="listing" class="text-lg" />
            <ListingAddress :listing="listing" class="text-gray-500" />
          </div>
        </Box>
      </div>
    </div>
  </template>
  
  <script setup>
  import ListingAddress from '@/Pages/Components/ListingAddress.vue'
  import ListingSpace from '@/Pages/Components/ListingSpace.vue'
  import Price from '@/Pages/Components/Price.vue'
  import Box from '@/Pages/Components/UI/Box.vue'
  
  defineProps({
    listing: Object,
  })
  </script>
  
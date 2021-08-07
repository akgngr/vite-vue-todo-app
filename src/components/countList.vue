<template>
    <p class="text-sm float-right pt-4 underline text-gray-600">Toplamda <span class="text-red-600 font-bold">{{ itemData.data.length }}</span> adet TODO var.</p>
</template>

<script>
export default {
    inject:['itemData']
}
</script>
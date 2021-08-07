<template>
    <ul class="pt-6">
        <li class="py-2 px-1 lg:py-1 lg:px-2 my-2 hover:bg-blue-50 border-dashed border-gray-100 border" v-for="item in itemData.data" :key="item.id">
            <div class="flex justify-between items-center">
                {{ item.title }}
                <button @click="deleteItem(item)" class="bg-red-500 text-white px-4 py-1 text-sm rounded-md">Sil</button>
            </div>
        </li>
    </ul>
</template>

<script>
export default {
    inject: ['itemData', 'deleteItem']
}
</script>
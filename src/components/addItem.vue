<template>
    <div class="pt-4">
      <input @keydown.enter="pushItem($event.target.value)" class="form-input px-3 py-2 w-full" placeholder="TODO Ekle" />
    </div>
</template>

<script>
export default {
    inject:['pushItem']
}
</script>
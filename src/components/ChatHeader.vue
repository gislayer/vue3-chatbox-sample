<template>
    <div class="card-header d-flex justify-content-between align-items-center p-3 bg-info text-white border-bottom-0"
        style="border-top-left-radius: 15px; border-top-right-radius: 15px;">
        <i class="fas fa-angle-left"></i>
        <p class="mb-0 fw-bold">{{ title }}</p>
        <i class="fas fa-times"></i>
    </div>
</template>

<script>
export default {
  name: "ChatHeader",
  inject:['title']
}
</script>

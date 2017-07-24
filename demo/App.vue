<template>
    <div id="app">
        <multiple-file-uploader postURL="" successMessagePath="" errorMessagePath=""></multiple-file-uploader>
    </div>
</template>

<script>
    import MultipleFileUploader from './../src/MultipleFileUploader.vue'

    export default {
        components: {
            MultipleFileUploader
        }
    }
</script>
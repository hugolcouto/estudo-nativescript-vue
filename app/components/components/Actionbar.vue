<template>
    <ActionBar 
        :title="title"
        textAlign="center"
        backgroundColor="#41b883"
        color="#fff"
    />
</template>

<script>
export default {
    props: ['title']
}
</script>
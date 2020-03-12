<template>
    <Page>
        <custom-actionbar :title="titleBar"/>
        <StackLayout>
            <Label :text="this.message" />
        </StackLayout>
    </Page>
</template>

<script>
export default {
    props: ['message', 'titleBar']
}
</script>
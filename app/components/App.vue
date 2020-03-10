<template>
    <Page>
        <ActionBar title="Welcome to NativeScript-Vue!"/>
        <StackLayout columns="*" rows="*">
            <Image src="~/assets/images/NativeScript-Vue.png" :style="{ marginTop: '20' }" />
            <ListView for="i in t">
                <v-template>
                    <Label :text="i" :style="{ padding: '0 20pt' }"/>
                </v-template>
            </ListView>
        </StackLayout>
    </Page>
</template>

<script >
  export default {
    data: () => ({
        msg: 'Hello World!',
        t: [1, 2, 3, 4]
    }),

    methods: {
        changeMessage(message) {
            this.msg = message;
        }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>

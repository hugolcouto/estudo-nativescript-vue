<template>
    <Page>
        <ActionBar title="Welcome to NativeScript-Vue!"/>
        <StackLayout columns="*" rows="*">
            <Label class="message" :text="msg" col="0" row="0"/>
            <Button 
                text="Change message" 
                backgroundColor="#41b883"
                color="#ffffff"
                @tap="changeMessage('Hello {N} Vue!')"
            />
            <Button 
                text="Original message" 
                backgroundColor="#41b883"
                color="#ffffff"
                @tap="changeMessage('Hello World!')"
            />
        </StackLayout>
    </Page>
</template>

<script >
  export default {
    data: () => ({
        msg: 'Hello World!'
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

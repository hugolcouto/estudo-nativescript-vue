<template>
    <Page>
        <custom-actionbar title="Olá mundo"/>
        <StackLayout columns="*" rows="*">
            <Image 
                src="~/assets/images/NativeScript-Vue.png"
                :style="{ margin: '20 0' }"
                width="60%"
            />
           <Button
                text="Hello World page"
                @tap="gotoHelloWorldPage"
           />
        </StackLayout>
    </Page>
</template>

<script>
    import HelloWorld from './views/HelloWorld';
    export default {
        methods: {
            gotoHelloWorldPage() {
                this.$navigateTo(HelloWorld, { props: { 
                        message: 'Eu vim da página principal',
                        titleBar: 'Exemplo de navegação'
                    }
                })
            }
        }
    }
</script>

<style scoped>
    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>

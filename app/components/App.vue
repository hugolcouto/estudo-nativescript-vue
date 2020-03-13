<template>
    <Page>
        <custom-actionbar title="Olá mundo"/>
        <StackLayout columns="*" rows="*">
            <SVGImage 
                src="~/assets/images/guntertux.svg"
                height="180"
            />
           <Button
                text="Hello World page"
                @tap="gotoHelloWorldPage"
                color="#fff"
                backgroundColor="#41b883"
           />
            <Button
                text="Modal page"
                @tap="gotoModalPage"
                color="#fff"
                backgroundColor="#41b883"
           />
        </StackLayout>
    </Page>
</template>

<script>
    import HelloWorld from './views/HelloWorld';
    import ModalExample from './views/ModalExample';
    export default {
        methods: {
            gotoHelloWorldPage() {
                this.$navigateTo(HelloWorld, { props: { 
                        message: 'Eu vim da página principal',
                        titleBar: 'Exemplo de navegação'
                    }
                })
            },
            gotoModalPage() {
                this.$showModal(ModalExample)
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

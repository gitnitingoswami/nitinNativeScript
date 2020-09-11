<template>
    <Page>
        <ActionBar title="Home" class="action" />
        <ScrollView>
            <StackLayout class="home-panel">
                <!--Add your page content here-->

                <Button class="btn-primary" text="Login" @tap="onButtonTap" />
                <Button class="btn-primary" text="Singup" @tap="Singup" />

            </StackLayout>
        </ScrollView>
    </Page>
</template>

<script>
    import Login from "./Login";
    import Singup from "./Singup";
    export default {
        methods: {
            onButtonTap() {
                this.$navigateTo(Login, {});
                console.log("Button was pressed");
            },
            Singup() {
                this.$navigateTo(Singup, {});
                console.log("press");
            }
        },

        data() {
            return {};
        }
    };
</script>

<style>
    ActionBar {
       background-color:red;
       
       color:white;
    }

    .home-panel {
        vertical-align: center;
        font-size: 20;
        margin: 15;
    }

    .description-label {
        margin-bottom: 15;
    }

    .btn-primary {
        height: 50;
        font-size: 20;
        font-weight: 600;
        background-color: red;
        color:white;
    }
</style>
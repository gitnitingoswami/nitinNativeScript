<template>
    <Page>
        <ActionBar title="Login" />


        <!--Add your page content here-->
        <FlexboxLayout class="page">
            <StackLayout class="form">
                <Label class="header" text="Login" />
                <Image class="image"
                    src="https://f1.pngfuel.com/png/933/945/137/social-media-icons-background-avatar-user-profile-login-black-circle-silhouette-symbol-png-clip-art.png" />

                <StackLayout class="input-field">
                    <TextField v-model="Username" class="input"
                        hint="Username..." />
                </StackLayout>

                <StackLayout class="input-field">
                    <TextField v-model="Password" secure="true" class="input"
                        hint="Password..." />
                </StackLayout>


                <Button text="Login" class="btn btn-primary"
                    @tap="onButtonTap" />
                <Button text="Dont have Account" class="btn btn-primary"
                    @tap="Account" />
            </StackLayout>

        </FlexboxLayout>


    </Page>
</template>

<script>
    import Singup from "./Singup";
    export default {
        methods: {
            onButtonTap() {
                console.log("Button was pressed");
            },
            Account() {
                this.$navigateTo(Singup, {});
            }
        },

        data() {
            return {
                Username: "",
                Password: ""
            };
        }
    };
</script>

<style>
    .page {
        align-items: center;

        font-size: 20;
        margin: 15;
    }

    .form {
        width: 100%;
        margin-left: 30;
        margin-right: 30;
        color: white;
    }

    .header {
        font-size: 25;
        text-align: center;
        color: red;
        font-weight: 600;
        margin-bottom: 30;
    }

    .image {
        width: 150;
        height: 150;
        border-radius: 100;
    }

    .input-field {
        margin-bottom: 20;

    }

    .input {
        font-size: 20;
    }

    .btn-primary {
        height: 50;
        background-color: red;
        font-size: 20;
        font-weight: 600;


    }
</style>
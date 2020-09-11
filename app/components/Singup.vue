<template>
    <Page>
        <ActionBar title="Singup" />


        <!--Add your page content here-->
        <FlexboxLayout class="page">
            <StackLayout class="form">
                <Label class="header" text="Singup" />
                <Image class="image"
                    src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcThYZdsBryWLe8RiNj5CaaKaiIZiQokNZM3ag&usqp=CAU" />
                <StackLayout class="input-field">
                    <TextField v-model="Fullname" class="input"
                        hint="Full name..." />
                </StackLayout>

                <StackLayout class="input-field">
                    <TextField v-model="Username" class="input"
                        hint="Username..." />
                </StackLayout>
                <StackLayout class="input-field">
                    <TextField v-model="Email" class="input"
                        keyboardType="email" hint="Email..." />
                </StackLayout>
                <StackLayout class="input-field">
                    <TextField v-model="Password" class="input"
                        hint="Password..." />
                </StackLayout>

                <StackLayout class="input-field">
                    <TextField v-model="Confirm" class="input"
                        hint="Confirm Password..." />
                </StackLayout>
                <Button text="Create Account" class="btn-primary"
                    @tap="onButtonTap" />

            </StackLayout>
        </FlexboxLayout>


    </Page>
</template>

<script>
    export default {
        methods: {
            onButtonTap() {
                console.log("Button was pressed");
            }
        },

        data() {
            return {
                Fullname: "",
                Username: "",
                Email: "",
                Password: "",
                Confirm: ""
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
    }

    .header {
        font-size: 25;
        text-align: center;
        color: red;
        font-weight: 600;
        margin-bottom: 20;
    }

    .image {
        border-radius: 100%;
        height: 150;
        width: 150;
    }

    .input-field {
        margin-bottom: 10;

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

    .btn-primary :hover {
        height: 50;
        color: green;
        background-color: red;
        font-size: 20;
        font-weight: 600;
    }
</style>
<template>
    <div class="flex justify-center">
        <form>
            <h1 class="p-2 m-2 text-3xl">Login!</h1>
            <div>
                <h2 class="p-2">Username</h2>
                <input type="text" value="" placeholder="Enter a valid username" class="rounded-lg border-2 p-2 m-2" />
            </div>

            <div>
                <h2 class="p-2">Password</h2>
                <input type="password" value="" placeholder="Enter a valid password"
                    class="rounded-lg border-2 p-2 m-2" />
            </div>

            <p class="text-red-600">{{ errorText }}</p>

            <button class="p-2 m-2 bg-black text-white rounded-lg" @click.prevent="validateForm">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'FormValidation',
    data() {
        return {
            username: "",
            password: "",
            errorText: ""
        }
    },
    methods: {
        validateForm() {
            const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
            if (this.username === '' || this.password === '') {
                this.errorText = 'Please enter missing values!';
            } else {
                this.errorText = "";
            }

            if (!emailPattern.test(this.username)) {
                this.errorText = "Invalid Username/Email";
            } else {
                this.errorText = "";
            }
        }
    }
}
</script>
<template>
    <div>
        <Navbar />

        <div class="container">
            <div class="card mt-5">
                <div class="card-header">Register</div>
                <div class="card-body">
                    <b-form @submit="onSubmit" v-if="show">
                        <b-form-group
                            id="name_label"
                            label="Full Name:"
                            label-for="name"
                        >
                            <b-form-input
                                id="name"
                                v-model="form.name"
                                placeholder="Enter your name"
                                required
                            ></b-form-input>
                        </b-form-group>

                        <b-form-group
                            id="email_label"
                            label="Email : "
                            type="text"
                            label-for="email"
                        >
                            <b-form-input
                                id="email"
                                v-model="form.email"
                                placeholder="Enter your Email"
                                required
                            ></b-form-input>
                        </b-form-group>

                        <b-form-group id="password_label" label="Password :" label-for="password">
                            <b-form-input
                                id="password"
                                v-model="form.password"
                                type="password"
                                placeholder="Enter your Password"
                                required
                            ></b-form-input>
                        </b-form-group>
                        
                        <b-button type="submit" variant="primary">Register</b-button>                    
                    </b-form>
                    <b-card class="mt-3" header="Form Data Result">
                        <pre class="m-0">{{ form }}</pre>
                    </b-card>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'

export default {
    components: {
        Navbar
    },
    data() {
        return {
            form: {
                name: "",
                email: "",
                password: "",
            },
            show: true,
        };
    },
    methods: {
        onSubmit(event) {
            event.preventDefault();
            alert(JSON.stringify(this.form));
        },
    },
};
</script>

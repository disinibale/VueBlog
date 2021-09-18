<template>
    <div>
        <b-navbar toggleable="lg" type="dark" variant="dark">
            <div class="container">
                <b-navbar-brand href="#">NavBar</b-navbar-brand>

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav>
                        <b-nav-item href="#">Link</b-nav-item>
                    </b-navbar-nav>

                    <b-navbar-nav class="ml-auto">
                        <b-nav-item>See Our Story</b-nav-item>
                        <b-nav-item>Write Your Story</b-nav-item>
                        <b-nav-item>Login</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </div>
        </b-navbar>
    </div>
</template>

<script>
export default {
    name: "Navbar",
};
</script>

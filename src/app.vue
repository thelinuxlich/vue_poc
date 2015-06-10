<style>
    html {
        font-family: Helvetica;
    }
    .blue {
        color: #69D2E7;
    }
</style>

<template>
    <h1 class="dork">This is the app</h1>
    <yb_cart custom="banana" dynamic="{{dynamic}}"></yb_cart>
    <yb_footer>
        <div>
            <strong>Custom content</strong>
        </div>
    </yb_footer>
    <yb_footer inline-template class="blue">
        <div class="blue">
            <strong>Here we are overwriting the whole footer template, but we still have access to its properties: {{msg}}</strong>
        </div>
    </yb_footer>
</template>

<script>
module.exports = {
    data: function() {
        return {
            dynamic: "Hello from App!"
        }
    },
    components: {
        yb_cart: require("./components/yb_cart.vue"),
        yb_footer: require("./components/yb_footer.vue")
    },
    created: function() {
        this.$on("yb_footer:ready", function(data) {
            console.log(data);
        });
    }
};
</script>
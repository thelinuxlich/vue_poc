<style>
.red {
    color: #f00;
}
</style>

<template>
    <div class="red">
        <h2>{{msg}}</h2>
        <content>This will be displayed if no content is inserted</content>
    </div>
</template>

<script>
module.exports = {
    data: function () {
        return {
            msg: 'Hello from Footer!'
        }
    },
    ready: function() {
        this.$dispatch("yb_footer:ready", "This event was fired when the yb_footer was fully initialized.");
    }
}
</script>
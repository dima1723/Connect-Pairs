<template>
    <div :class="'board-item ' + (selected ? 'selected' : '') + (closed ? 'closed' : '')">
        <i v-if="icon" :class="'icon icon-' + icon"></i>
    </div>
</template>

<script>


export default {
    name: 'BoardItem',

    props: {
        icon: {
            type: Number,
            required: false,
            default: 0,
        },
        selected: {
            type: Boolean,
            required: false,
            default: false,
        },
        closed: {
            type: Boolean,
            required: false,
            default: false,
        }
    }
}
</script>

<style>
 .board-item {
    border: 1px solid #2c3e50;
    width: 48px;
    height: 48px;
    position: relative;
 }

 .selected {
    background-color: #00ff0077;
 }

 .closed {
    background-color: #00ff0040;
 }

.icon {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

 .icon-1 {
    background: url('../assets/free-icon-apple-1791305.png');
    background-size: 50px 50px;

    background-position: 0 0;
 }

 .icon-2 {
    background: url('../assets/free-icon-banana-4899138.png');
    background-size: 50px 50px;

    background-position: 50px 0;
 }

 .icon-3 {
    background: url('../assets/free-icon-blueberry-1791354.png');
    background-size: 50px 50px;

    background-position: 100px 0;
 }

 .icon-4 {
    background: url('../assets/free-icon-cherry-1791306.png');
    background-size: 50px 50px;

    background-position: 100px 0;
 }

 .icon-5 {
    background: url('../assets/free-icon-grape-1412542.png');
    background-size: 50px 50px;

    background-position: 100px 0;
 }

 .icon-6 {
    background: url('../assets/free-icon-strawberry-1791343.png');
    background-size: 50px 50px;

    background-position: 100px 0;
 }
</style>
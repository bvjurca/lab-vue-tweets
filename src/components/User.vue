<template>
    <span class="name"> {{ user.name }} </span>
    <span class="handle">  {{ user.handle }} </span>
</template>

<script>

export default {
    props: {
        user: {
            name: String,
            handle: String,
        },
    },
};

</script>

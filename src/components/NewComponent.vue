<template>
    <div>
        {{ name }}
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true
        }
    },
    setup(props) {
        const { name } = props;
        return {
            name
        }
    }
}
</script>

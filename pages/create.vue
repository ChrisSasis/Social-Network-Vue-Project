<template>
    <div>
        <headerSecondary/>
        <createPost/>
    </div>
</template>

<script>
import headerSecondary from '~/components/Nav/headerSecondary';
import createPost from '~/components/Post/createPost';

export default {
    name: "create",
    components : {
        createPost,
        headerSecondary
    }
}
</script>
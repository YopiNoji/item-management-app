<template>
    <div>
        <Header></Header>
        <router-view></router-view>
    </div>
</template>

<script>
import Header from "./components/Layout/Header";

export default {
    components: {
        Header,
    },
    created() {
        this.$store.dispatch("Auth/setUserInfo");
    },
};
</script>

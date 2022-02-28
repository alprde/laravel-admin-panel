<template>
    <Head>
        <title>Dashboard</title>
    </Head>

    <Header>
        <h2 class="font-semibold text-xl text-gray-800 leading-tight">
            Dashboard
        </h2>
    </Header>

    <Main>
        <welcome />
    </Main>
</template>

<script>
    import { defineComponent } from 'vue'
    import Welcome from '@/Jetstream/Welcome.vue'
    import Header from "@/Shared/Header";
    import Main from "@/Shared/Main";

    export default defineComponent({
        components: {
            Welcome,
            Header,
            Main
        },
    })
</script>

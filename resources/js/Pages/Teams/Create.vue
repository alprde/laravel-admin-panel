<template>
    <Head>
        <title>Create Team</title>
    </Head>

    <Header>
        <h2 class="font-semibold text-xl text-gray-800 leading-tight">
            Create Team
        </h2>
    </Header>

    <div>
        <div class="max-w-7xl mx-auto py-10 sm:px-6 lg:px-8">
            <create-team-form />
        </div>
    </div>
</template>

<script>
    import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'
    import CreateTeamForm from '@/Pages/Teams/Partials/CreateTeamForm.vue'
    import Header from "@/Shared/Header";

    export default defineComponent({
        components: {
            Header,
            AppLayout,
            CreateTeamForm,
        },
    })
</script>

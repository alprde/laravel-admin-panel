<template>
<!--    <Head :title="title" />-->

    <jet-banner />

    <div>
        <div class="min-h-screen bg-gray-100">
            <Nav></Nav>

            <!-- Page Heading -->
<!--            <header class="bg-white shadow" v-if="$slots.header">-->
<!--                <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">-->
<!--                    <slot name="header"></slot>-->
<!--                </div>-->
<!--            </header>-->

            <!-- Page Content -->
            <main>
                <slot></slot>
            </main>
        </div>
    </div>
</template>

<script>
    import { defineComponent } from 'vue'
    import JetBanner from '@/Jetstream/Banner.vue'
    import Nav from "@/Shared/Nav";
    import Header from "@/Shared/Header";
    import Main from "@/Shared/Main";

    export default defineComponent({
        props: {
            title: String,
        },

        components: {
            Nav,
            JetBanner,
            Header,
            Main
        },

        data() {
            return {
                showingNavigationDropdown: false,
            }
        },

        methods: {
            switchToTeam(team) {
                this.$inertia.put(route('current-team.update'), {
                    'team_id': team.id
                }, {
                    preserveState: false
                })
            },

            logout() {
                this.$inertia.post(route('logout'));
            },
        }
    })
</script>

<template>
    <div>
        <div :class="this.sidebarOpen ? 'block' : 'hidden'" @click="this.sidebarOpen = false"
             class="fixed z-20 inset-0 bg-black opacity-50 transition-opacity lg:hidden"></div>
        <div :class="this.sidebarOpen ? 'translate-x-0 ease-out' : '-translate-x-full ease-in'"
             class=" h-screen fixed z-30 inset-y-0 left-0 w-64 transition duration-300 transform bg-gray-800 overflow-y-auto lg:translate-x-0 lg:static lg:inset-0">

            <nav class="mt-10">
                <a class="flex items-center mt-4 py-2 px-6 bg-gray-700 bg-opacity-25 text-gray-100" href="/">
                    <span class="mx-3">Tickets</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/ui-elements">

                    <span class="mx-3">Ideas</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/tables">
                    <span class="mx-3">Contacts</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/forms">

                    <span class="mx-3">Agents</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/forms">

                    <span class="mx-3">Articles</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/forms">

                    <span class="mx-3">Settings</span>
                </a>

                <a class="flex items-center mt-4 py-2 px-6 text-white hover:bg-gray-600 hover:bg-opacity-25 hover:text-gray-100"
                   href="/forms">
                    <font-awesome-icon icon="user-secret" />
                    <span class="mx-3">Subscription</span>
                </a>

            </nav>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            sidebarOpen: false
        };
    },
};
</script>

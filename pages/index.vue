<template>
    <div>
        <div class="px-6">
            <div class="flex flex-col">
                <div class=" py-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
                    <div
                        class="align-middle inline-block min-w-full shadow overflow-hidden sm:rounded-lg border-b border-gray-200">


                        <table class="min-w-full">
                            <thead class="bg-white border-b-2 border-gray-200">
                            <tr>
                                <th scope="col"
                                    class="px-6 py-3 text-left text-xs font-medium text-gray-500 tracking-wider">
                                    Ticket details
                                </th>
                                <th scope="col"
                                    class="px-6 py-3 text-left text-xs font-medium text-gray-500 tracking-wider">
                                    Customer name
                                </th>
                                <th scope="col"
                                    class="px-6 py-3 text-left text-xs font-medium text-gray-500 tracking-wider">
                                    Date
                                </th>
                                <th scope="col"
                                    class="px-6 py-3 text-left text-xs font-medium text-gray-500 tracking-wider">
                                    Priority
                                </th>
                            </tr>
                            </thead>
                            <tbody class="bg-white divide-y divide-gray-200">
                            <tr v-for="item in userDatas.data">
                                <td class="px-6 py-4 whitespace-nowrap">
                                    <div class="flex items-center">
                                        <div class="flex-shrink-0 h-10 w-10">
                                            <img class="h-10 w-10 rounded-full" v-bind:src=item.avatar alt="">
                                        </div>
                                        <div class="ml-4">
                                            <div class="text-sm font-medium text-gray-900">
                                                {{ item.first_name }}
                                            </div>
                                            <div class="text-sm text-gray-500">
                                                {{ item.email }}
                                            </div>
                                        </div>
                                    </div>
                                </td>

                                <td class="px-6 py-4 whitespace-nowrap">
                                    <div class="text-sm text-gray-900">Regional Paradigm Technician</div>
                                    <div class="text-sm text-gray-500">Optimization</div>
                                </td>

                                <td class="px-6 py-4 whitespace-nowrap">
                                    <span
                                        class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800">
                                      Active
                                    </span>
                                </td>

                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
                                    Admin
                                </td>

                            </tr>
                            </tbody>
                        </table>
                        <div class="bg-white border-t-2 flex justify-end p-5">
                            <p class="text-gray-700"> 1 - {{ userDatas.per_page }} of {{ userDatas.total }}</p>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>


export default {
    data() {
        return {
            userDatas: {}
        };
    },
    async asyncData({$axios}) {
        const userDatas = await $axios.$get('/users?page=2')
        return {userDatas}
    },
};
</script>

<style></style>

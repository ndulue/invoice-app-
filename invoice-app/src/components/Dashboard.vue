<template>
    <div>
        <div class="container-fluid" style="padding: 0px"></div>
        <Header v-bind:user="user"/>
        <template v-if="this.isactive == 'create'">
            <CreateInvoice></CreateInvoice>
        </template>
        <template v-else>
            <ViewInvoices/>
        </template>
    </div>
</template>

<script>
import Header from './Header';
import CreateInvoice from './CreateInvoice';
import ViewInvoices from './ViewInvoices';
export default {
    name: "Dashboard",
    components: {
        Header,
        CreateInvoice,
        ViewInvoices
    },
    data() {
        return {
            isactive : 'create',
            title : "Invoice app",
            user : (this.$route.params.user) ? this.$route.params.user : null
        };
    },
};
</script>
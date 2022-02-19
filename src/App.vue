<template>
<section>
<h2>My Friends</h2>
<ul>
<FriendContact name="Manual Lorez" phone-number="424-8942" email-address="manuel@localhost.com"></FriendContact>
<FriendContact name="JulieJoens" phone-number="20-249-24" email-address="julie@localhost.com"></FriendContact>
</ul>


</section>

</template>
<script>
import FriendContact from "./components/FriendContact.vue";

    export default{
    data() {
        return {
            friends: [
                {
                    id: "manual",
                    name: "Manual Lorenz",
                    phone: "0123 45678 90",
                    email: "manual@localhost.com"
                },
                {
                    id: "julie",
                    name: "julie Jones",
                    phone: "0987 654421 21",
                    email: "julie@localhost.com"
                },
            ]
        };
    },
    methods: {},
    computed: {},
    components: { FriendContact }
}


</script>
<style>


</style>
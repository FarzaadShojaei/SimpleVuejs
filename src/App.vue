<template>
<section>
<h2>My Friends</h2>
<ul>
<FriendContact v-for="friend in friends" 
:key="friend.id" 
:id="friend.id"
:name="friend.name"
 :phone-number="friend.phone" 
 :email-address="friend.email" 
 :is-favorite="friend.isFavorite"
 @toggle-favorite="toggleFavoriteStatus"></FriendContact>
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
                    email: "manual@localhost.com",
                    isFavorite:true
                },
                {
                    id: "julie",
                    name: "julie Jones",
                    phone: "0987 654421 21",
                    email: "julie@localhost.com",
                    isFavorite:false
                },
            ],
        };
    },
    methods: {
        toggleFavoriteStatus(friendId){
           const identifiedFriend= this.friends.find((friend) => friend.id === friendId);
           identifiedFriend.isFavorite=!identifiedFriend.isFavorite;
        }
    },
    computed: {},
    components: { FriendContact }
}


</script>
<style>


</style>
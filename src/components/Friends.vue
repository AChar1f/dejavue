<template>
    <div class="row justify-content-center">
        <div class="row">
            <h2 class="display-2">Friends</h2>
        </div>
        <div class="row justify-content-center gap-3" v-if="friends.length">
            <Card v-for="(friend, id) in friends" :key="id" :class="{
        male : friend.gender.toLowerCase() == 'male', 
        female : friend.gender.toLowerCase() == 'female'
        }">
            <template #cardHeader>
            <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy">
            </template>
            <template #cardBody>
            <h5>{{ friend.firstName }} {{ friend.lastName }}</h5>
            <h6>{{ friend.gender }}</h6>
            </template>
        </Card>
        </div> 
        <div class="row justify-content-center pt-3" v-else>
            <div class="honeycomb">
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                </div>
         </div>    
    </div>
  </template>
  
  
  <script>
import Card from './Card.vue'
  
  export default {
    name: 'FriendsComp',
    components: {Card},
    data() {
    return {
      friends : [
      {
      id: 1,  
      firstName: 'Mustafa',
      lastName: 'Moerat',
      gender: 'Male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 2,
      firstName: 'Qaasiem',
      lastName: 'Harliem',
      gender: 'Male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 3,
      firstName: 'Nasief',
      lastName: 'Isaacs',
      gender: 'Male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 4,
      firstName: 'Saabir',
      lastName: 'Adams',
      gender: 'Male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 5,  
      firstName: 'Azeez',
      lastName: 'Busack',
      gender: 'Male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 6,  
      firstName: 'Aneeqah',
      lastName: 'Busack',
      gender: 'Female',
      profile: 'https://achar1f.github.io/projectimages/images/f-profile.png'
    }
  ]
    }
  }
  } 

  </script>
  

  <style scoped>
.male {
  border: 6px solid gold;
  background-color:paleturquoise;
}
.female{
  border:6px solid pink;
  background-color:violet;
}

@-webkit-keyframes honeycomb {
  0%,
  20%,
  80%,
  100% {
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
  }

  30%,
  70% {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes honeycomb {
  0%,
  20%,
  80%,
  100% {
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
  }

  30%,
  70% {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

.honeycomb {
  height: 24px;
  position: relative;
  width: 24px;
}

.honeycomb div {
  -webkit-animation: honeycomb 2.1s infinite backwards;
  animation: honeycomb 2.1s infinite backwards;
  background: silver;
  height: 12px;
  margin-top: 6px;
  position: absolute;
  width: 24px;
}

.honeycomb div:after, .honeycomb div:before {
  content: '';
  border-left: 12px solid transparent;
  border-right: 12px solid transparent;
  position: absolute;
  left: 0;
  right: 0;
}

.honeycomb div:after {
  top: -6px;
  border-bottom: 6px solid silver;
}

.honeycomb div:before {
  bottom: -6px;
  border-top: 6px solid silver;
}

.honeycomb div:nth-child(1) {
  -webkit-animation-delay: 0s;
  animation-delay: 0s;
  left: -28px;
  top: 0;
}

.honeycomb div:nth-child(2) {
  -webkit-animation-delay: 0.1s;
  animation-delay: 0.1s;
  left: -14px;
  top: 22px;
}

.honeycomb div:nth-child(3) {
  -webkit-animation-delay: 0.2s;
  animation-delay: 0.2s;
  left: 14px;
  top: 22px;
}

.honeycomb div:nth-child(4) {
  -webkit-animation-delay: 0.3s;
  animation-delay: 0.3s;
  left: 28px;
  top: 0;
}

.honeycomb div:nth-child(5) {
  -webkit-animation-delay: 0.4s;
  animation-delay: 0.4s;
  left: 14px;
  top: -22px;
}

.honeycomb div:nth-child(6) {
  -webkit-animation-delay: 0.5s;
  animation-delay: 0.5s;
  left: -14px;
  top: -22px;
}

.honeycomb div:nth-child(7) {
  -webkit-animation-delay: 0.6s;
  animation-delay: 0.6s;
  left: 0;
  top: 0;
}
  </style>
  
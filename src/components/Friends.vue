<template>
    <div class="row">
        <h2>Friends</h2>
      <Card v-for="(friend, id) in friends" :key="id">
        <template #cardHeader>
          <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy">
        </template>
        <template #cardBody>
          <h5>{{ friend.firstName }} {{ friend.lastName }}</h5>
          <h6>{{ friend.gender }}</h6>
        </template>
      </Card>
    </div>
  </template>
  
  
  <script>
import Card from '@/components/Card.vue'
  
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
      gender: 'male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 2,
      firstName: 'Qaasiem',
      lastName: 'Harliem',
      gender: 'male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 3,
      firstName: 'Nasief',
      lastName: 'Isaacs',
      gender: 'male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 4,
      firstName: 'Saabir',
      lastName: 'Adams',
      gender: 'male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 5,  
      firstName: 'Ismaeel',
      lastName: 'Ahmed',
      gender: 'male',
      profile: 'https://achar1f.github.io/projectimages/images/profile.jpg'
    },
    {
      id: 6,  
      firstName: 'Aneeqah',
      lastName: 'Busack',
      gender: 'female',
      profile: 'https://achar1f.github.io/projectimages/images/f-profile.png'
    }
  ]
    }
  }
  } 

  </script>
  

  <style scoped>

  </style>
  
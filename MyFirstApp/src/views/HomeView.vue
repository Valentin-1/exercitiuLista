<script>
export default{
  data(){
    return{
      infoList: [
        {
          id: 1,
          nume: "Andrei",
          phone: "06934324",
          email: "ion@gmail.com"
        },
        {
          id: 2,
          nume: "Cristian",
          phone: "06937543",
          email: "andr@gmail.com"
        },
        {
          id: 3,
          nume: "Jhon",
          phone: "069356564",
          email: "omar@gmail.com"
        },
      ],
      resultList: [],
      show: false
    }
  },
  methods: {
    openInfo(){
      this.show = !this.show
      
    }
  }
}
</script>

<template>
  <div id="information">
    <ul>
      <li v-for="item in infoList" :key="item.id" @click="openInfo()" >
        {{ item.nume }}
      </li>
    </ul>
    <div v-for="index in infoList" :key="index.nume">
        <div v-show="this.show" >
          Phone: {{ index.phone }} <br/>
          Email: {{ index.email }}
        </div>
    </div>
  </div>
</template>
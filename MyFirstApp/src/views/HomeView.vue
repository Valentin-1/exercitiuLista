<script>
export default{
  data(){
    return{
      infoList: [
        {
          id: 1,
          nume: "Andrei Ionescu",
          age: "18",
          phone: "06934324",
          email: "ion@gmail.com"
        },
        {
          id: 2,
          nume: "Cristian Petrscu",
          age: "25",
          phone: "06937543",
          email: "andr@gmail.com"
        },
        {
          id: 3,
          nume: "Jhon Smit",
          age: "30",
          phone: "069356564",
          email: "omar@gmail.com"
        },
      ],
      resultList: [],
      show: null,
      isVisibil: false,
    }
  },
  methods: {
    openInfo(id){
      this.show = id
      this.isVisibil = !this.isVisibil
    }
  }
}
</script>

<template>
  <div id="information">
    <div id="styleList">
      <ul id="list">
        <li id="key" v-for="item in infoList" :key="item.id" @click="openInfo(item.id)" >
          {{ item.nume }}
        </li>
      </ul>
    </div>

    <div  v-for="index in infoList" :key="index.nume">
        <div id="info" v-show="show === index.id && this.isVisibil" >
          Age: {{index.age}} <br>
          Phone: {{ index.phone }} <br/>
          Email: {{ index.email }} 

        </div>
    </div>
  </div>
</template>

<style>
#list{
  list-style-type: none;
}

#key:hover{
  border: 2px solid red;
  width: 120px;
}

#styleList{
 border: 2px solid black;
 width: 170px;
}

#information{
  display: flex;
}

#info{
  border: 2px solid blue;
  height: 100px;
  width: 200px;
}
</style>
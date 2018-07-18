<template>
<div id="test">
<ul><li><a @click="showdetail('球类')">球类</li>
    <li><a @click="showdetail('粮食')">粮食</li>
    <li><a @click="showdetail('衣服')">衣服</li>
</ul>
<ul v-for="item in arr" :key="item.id">
         <li>item.src</li>
         <li>item.price</li>
         <li>item.msg</li>
</ul>
</div>
</template>

<script>
export default {
  data() {
    return {
        arr=[],
      obj: {
        球类: [
          {id:1, src: "../image/football.jpg", price: 10, msg: "足球" },
          { id:2,src: "../image/basketball.jpg", price: 20, msg: "篮球" },
          { id:3,src: "../image/tennis.jpg", price: 30, msg: "乒乓球" }
        ],
        粮食: [
          {id:1, src: "../image/husked.jpg", price: 20, msg: "大米" },
          { id:2,src: "../image/corn.jpg", price: 5, msg: "玉米" },
          { id:3,src: "../image/mung.jpg", price: 10, msg: "绿豆" }
        ],
        衣服: [
          { id:1,src: "../image/T.jpg", price: 40, msg: "T恤" },
          { id:2,src: "../image/sports.jpg", price: 60, msg: "运动服" },
          { id:3,src: "../image/coat.jpg", price: 50, msg: "外套" }
        ]
      }
    };
  },
  methods: {
    showdetail(cmsg){
   this.arr=obj[cmsg]
    }
  },

  components: {},

  computed: {},

  mounted() {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

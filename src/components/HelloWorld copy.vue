<template>
  <div class="container">
    <div class="page">
      <div class="hello">
        <div class="hello_txt">
          <h1>夏日慶典</h1>
          <h2>史上最可愛的浴衣女孩跟你一起</h2>
          <h3 class="substribe">當主角了喔</h3>
        </div>
        <img
          src="../assets/item_sub00101_sp.png"
          alt=""
          srcset=""
          class="sp01 sp"
        />
        <img
          src="../assets/item_sub00102_sp.png"
          alt=""
          srcset=""
          class="sp02 sp"
        />
      </div>
      <div class="hello"></div>
      <div class="hello"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
 
.main::-webkit-scrollbar {
  width: 0px; 
  height: 0px;
}
/*滾動條裡面小方塊樣式*/

.main::-webkit-scrollbar-thumb { 
  box-shadow: inset 0 0 1px rgba(0, 0, 0, 0.2);
}
*{
  scroll-behavior: smooth;
  overflow-x: hidden;
}
#app {
  margin: 0;
  padding: 0; 
  overflow: hidden;
}
.page { 
  overflow-x: scroll;
  display: inline-flex;
}

.hello {
  display: inline-flex;
  background: yellow;
  height: 100vh;
  width: 100vw;
  background: url("../assets/ppt.png");
  position: relative;
  overflow:hidden;
}
h1 {
  font-size: 65px;
}
.sp {
  height: 90vh;
}
.sp01 {
  position: absolute;
  left: -50px;
  bottom: 0;
}
.sp02 {
  position: absolute;
  right: -50px;
  bottom: 0;
}
.hello_txt {
  text-align: right;
  position: absolute;
  left: 50%;
  top: 30%;
  transform: translate(-50%, -50%);
}
.substribe {
  font-weight: bold;
  font-size: 20px;
}
h3 {
  margin: 40px 0 0;
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
<script>
let sp01 = document.getElementById("sp01");
document.addEventListener("mousedown", function () {
  let postion = function () {
    return {
      left:
        (document.documentElement && document.documentElement.scrollLeft) ||
        document.body.scrollLeft,
      top:
        (document.documentElement && document.documentElement.scrollTop) ||
        document.body.scrollTop,
    };
  };
  console.log(scroll);
});
</script>

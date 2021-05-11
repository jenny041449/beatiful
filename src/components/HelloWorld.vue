<template>
  <div id="container">
    <div id="container2">
      <!-- <div class="box one" style="border:1px soild red"> 2 </div> -->
      <div class="box two">
        <div class="hello_txt" id="hello_txt">
          <h1>夏日慶典</h1>
          <h2>史上最可愛的浴衣女孩跟你一起</h2>
          <h3 class="substribe">當主角了喔</h3>
        </div>
        <img
          src="../assets/item_sub00101_sp.png"
          alt=""
          srcset=""
          class="sp01 sp"
          id="sp01"
        />
        <img
          src="../assets/item_sub00102_sp.png"
          alt=""
          srcset=""
          class="sp02 sp"
          id="sp02"
          @click="run"
        />
        <div class="two">
          <div>
            <img src="../assets/p2.png" alt="" srcset="" class="sp02 asp2" id="asp2" @click="reset()"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// let sp01 = document.querySelector(".sp01");
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {
    run() {
      document
        .querySelector("#sp01")
        .setAttribute("style", "transform:translate(-50%,-200%)");

      document
        .getElementById("sp02")
        .setAttribute("style", "right:50%;transform:translatX(100%)");
      document
        .querySelector("#hello_txt")
        .setAttribute("style", "transform:translate(-50%,-200%)");

      document.getElementById("asp2").setAttribute("style", "opacity:1;height: 80%;");
    },
    reset(){
      document
        .querySelector("#sp01")
        .setAttribute("style", "transform:translate(0%,0%)");

      document
        .getElementById("sp02")
        .setAttribute("style", "right:0;transform:translatX(0%)");
      document
        .querySelector("#hello_txt")
        .setAttribute("style", "transform:translate(-50%,-50%)");

      document.getElementById("asp2").setAttribute("style", "opacity:0;height: 0;");

    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
/* .main::-webkit-scrollbar {
  width: 1px   !important; 
  height: 1px  !important;
  } */
/*滾動條裡面小方塊樣式*/
/*  
.main::-webkit-scrollbar-thumb { 
  box-shadow: inset 0 0 1px rgba(0, 0, 0, 0.2);
} */

.sp {
  height: 80vh;
}
.sp01 {
  position: absolute;
  left: -50px;
  bottom: 0;
  transition: 3s;
}
.sp01:hover,.sp02:hover,.asp2:hover {
  opacity: 0.7;
}
.sp02 {
  position: absolute;
  right: -50px;
  bottom: 0;
  transition: 8s;
}
.hello_txt {
  border: 10px solid rgb(74, 204, 243);
  background: rgb(255, 255, 234);
  font-size: 35px;
  height: 500px;
  color: rgb(197, 20, 14);
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-100%, -50%);
  transition: 12s linear;
}
.substribe {
  font-weight: bold;
  font-size: 20px;
}
body {
  margin: 0;
  font-family: Georgia;
}
#container .box {
  width: 100vw;
  height: 100vh;
  display: inline-block;
  position: relative;
}
.hello_txt {
  text-align: right;
  position: absolute;
  left: 50%;
  top: 30%;
  transform: translate(-50%, -50%);
  transition: 3s;
}
#container {
  overflow-y: scroll;
  overflow-x: hidden;
  transform: rotate(270deg) translateX(-100%);
  transform-origin: top left;
  background-color: rgb(250, 249, 211);
  position: absolute;
  width: 100vh;
  height: 100vw;
}
#container2 {
  transform: rotate(90deg) translateY(-100vh);
  transform-origin: top left;
  white-space: nowrap;
  font-size: 0;
}
.box {
  display: inline-flex;
  background: yellow;
  height: 100vh;
  width: 100vw;
  background: url("../assets/ppt.png");
  position: relative;
  overflow: hidden;
  animation: 10s 2s gogo infinite both linear;
}
@keyframes gogo {
  0% {
    background-position: -10% -10%;
  }
  25% {
    background-position: 0% 0%;
  }
  50% {
    background-position: -10% -10%;
  }
}
/*two  */
.asp2 {
  opacity: 0;
  height: 0%;
  position: absolute;
  right: 10%;
  bottom: 30px;
  transition: 12s opacity;
}
</style>

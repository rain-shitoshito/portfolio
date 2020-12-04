<template>
  <div id="email" class="w-100 h-100">
    <p class="text-center relative mb-0"><i class="brank before"></i><span id="spam">takuma.maeda</span>axas-japan.co.jp<i class="brank after"></i></p>
  </div>
</template>
<style scoped>
#spam::after {
  content: '@';
  color: blue;
}
#email {
  display: flex;
  align-items: center;
  justify-content: center;
}
.brank {
  width: 50px;
  height: 1px;
  background-color:#d5dde3;
  position: absolute;
}
.brank.before {
  top: -10px;
  left: -30px;
}
.brank.after {
  bottom: -10px;
  right: -30px;
}
.brank.before::before {
  content: "";
  width: 1px;
  height: 50px;
  background-color:#d5dde3;
  position: absolute;
  top: -25px;
  left: 15px;
}
.brank.after::before {
  content: "";
  width: 1px;
  height: 50px;
  background-color:#d5dde3;
  position: absolute;
  bottom: -25px;
  right: 15px;
}
</style>
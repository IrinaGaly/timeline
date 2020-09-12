<template>
  <div class="timeline">
    <div class="container left">
      <div class="content">
        <timelineBox />
      </div>
    </div>
  <!-- <div class="container right">
    <div class="content">
      <ul class="content__list">
        <li class="contetn__item">
          <h2 class="name">2017</h2>
          <p class="about">Lorem ipsum..</p>
          <div class="registered"></div>
          <div class="tags">
            <span>{{tags}}</span>
          </div>
        </li>
      </ul>
    </div>
  </div> -->
  </div>
</template>

<script>
import timelineBox from "./components/timelineBox/timelineBox"

export default {
  name: 'app',
  components: {
    timelineBox
  },

  data() {
    return {

    }
  },
  created() {
  
  }
}
</script>

<style lang="scss">
  * {
  box-sizing: border-box;
}

body {
  background-color: #A0522D;
  font-family: Helvetica, sans-serif;
}

ul {
  list-style: none;
}
.timeline {
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
}

.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: white;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

.container {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 50%;
}

.container::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -17px;
  background-color: white;
  border: 4px solid #FF9F55;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

.left {
  left: 0;
}

.right {
  left: 50%;
}

.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid white;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent white;
}

.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid white;
  border-width: 10px 10px 10px 0;
  border-color: transparent white transparent transparent;
}

.right::after {
  left: -16px;
}

.content {
  padding: 20px 30px;
  background-color: white;
  position: relative;
  border-radius: 6px;
}

@media screen and (max-width: 600px) {
  .timeline::after {
    left: 31px;
  }


  .container {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }


  .container::before {
    left: 60px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
  }


  .left::after, .right::after {
    left: 15px;
  }


  .right {
    left: 0%;
  }
}
</style>

<template>
  <div id="app">
    <div class="log-in">
      <div class="container-fluid mt-4">
        <div class="row">
          <div class="col"></div>
          <div class="col justify-content-center">
            <HelloWorld :card="author[counter]" />
            <button type="button" class="btn btn-primary" :disabled="isFirst()" @click="decCounter()">Prev</button>
            <button type="button" class="btn btn-primary" :disabled="isLast()" @click="incCounter()">Next</button>
          </div>
          <div class="col"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      counter: 0,
      author: [
        {
          name: "Dennis",
          age: 21,
          msg: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          img: require("../src/assets/man_1.jpg")
        },
        {
          name: "Ivan",
          age: 15,
          msg: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Nibh ipsum consequat nisl vel pretium lectus. Aliquam malesuada bibendum arcu vitae elementum curabitur vitae. Leo vel fringilla est ullamcorper eget nulla facilisi. Enim ut tellus elementum sagittis vitae. Pretium fusce id velit ut tortor pretium viverra. Odio eu feugiat pretium nibh ipsum consequat nisl. Sit amet risus nullam eget felis. Pulvinar pellentesque habitant morbi tristique. Pharetra pharetra massa massa ultricies. Vulputate mi sit amet mauris commodo quis. Erat pellentesque adipiscing commodo elit at imperdiet dui accumsan sit. Blandit massa enim nec dui nunc. Nulla aliquet enim tortor at auctor urna nunc. Egestas diam in arcu cursus euismod quis. At in tellus integer feugiat scelerisque.",
          img: require("../src/assets/man_2.jpg")
        },
        {
          name: "John",
          age: 34,
          msg: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. A diam sollicitudin tempor id eu nisl nunc mi. Tristique senectus et netus et malesuada fames. A arcu cursus vitae congue mauris rhoncus aenean vel. Ornare massa eget egestas purus viverra accumsan in. Donec ac odio tempor orci dapibus ultrices in iaculis. Egestas congue quisque egestas diam in arcu cursus euismod quis. Nisl nunc mi ipsum faucibus vitae. Vel risus commodo viverra maecenas accumsan lacus. Tempor orci eu lobortis elementum nibh. Elementum curabitur vitae nunc sed velit dignissim sodales ut eu. Nunc vel risus commodo viverra maecenas accumsan. Nullam eget felis eget nunc lobortis mattis aliquam faucibus purus. Libero id faucibus nisl tincidunt eget nullam non. Laoreet non curabitur gravida arcu ac tortor. Tincidunt dui ut ornare lectus sit amet. Placerat orci nulla pellentesque dignissim.",
          img: require("../src/assets/man_3.jpg")
        },
      ]
    }
  },
  methods: {
    incCounter(){
      if (this.counter + 1 < this.author.length)
        this.counter++
    },
    decCounter(){
      if (this.counter - 1 >= 0)
        this.counter--
    },
    isLast(){
      return this.counter === this.author.length - 1
    },
    isFirst(){
      return this.counter === 0
    },
  }
}
</script>

<style>
@import 'https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css';
</style>

<template>
  <h2>Counter!!</h2>
  <p>{{counter}} <sup>2</sup>= {{ squareCounter }} -1</p>


  <div>
    <button>+1</button>
    <button>-1</button>
  </div>

</template>

<script>
export default {
    data() {
        return {
            counter: 10
        }
    },
    methods: {
        getSquareValue () {
            console.log("getSquareValue()")
            return this.counter * this.counter
        }
    },
    computed: {
        squareCounter() {
            console.log("Computed Square Counter")
            return this.counter * this.counter
        }
    }
}
</script>

<style>

button {
    background-color: #64bbb7;
    border-radius: 5px;
    border: 1px solid white;
    color: white;
    cursor: pointer;
    margin: 0 5px;
    padding: 5px 15px;
    transition: 0.3s ease-in-out;

}

button:hover {
    background-color: #5aa67b;
    transition: 0.3s ease-in-out;
}


</style>
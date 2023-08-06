<template>
  <div class="hello">
    <div>
      <h1>{{ msg }}</h1>
      <div class="card-holder">
        <div class="card" v-for="(KodehauzStaff, index) in KodehauzStaffs" :key="index">
          <h3 class="text">Name: {{KodehauzStaff.name}}</h3>
          <p class="text">Gender: {{KodehauzStaff.gender}}</p>
          <p class="text">Role: {{KodehauzStaff.role}}</p>
          <p class="text">Complexion: {{KodehauzStaff.complexion}}</p>
        </div>
      </div>
    </div>
    <div class="sec">
      <h1>Word Reverse</h1>
      <div>
        {{text}}
        <button @click="reverse">ffff</button>
      </div>
    </div>
    <div class="sec">
      <h1>Text Color Change</h1>
      <div>
        <h1> count is: {{ count }} </h1>
        <button @click="increseCount" class="btn btn-primary">count</button> 
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
   return {
    count: 0,
    KodehauzStaffs: [
      {name: 'Joshua', gender: 'Male', role: 'Beginner Web developer Mentor', complexion: 'Fair'},
      {name: 'Ogochuku', gender: 'Male', role: 'Advance Web developer Mentor', complexion: 'Fair'},
      {name: 'Victor', gender: 'Male', role: 'CAD Mentor', complexion: 'Dark'},
      {name: 'Nsisong', gender: 'Male', role: 'IOT Mentor', complexion: 'Fair'},
      {name: 'Favour', gender: 'Female', role: 'UI/UX Mentor', complexion: 'Fair'},
      {name: 'Ihechi', gender: 'Male', role: 'Assistance UI/UX Mentor', complexion: 'Fair'},
      {name: 'Kingsley', gender: 'Male', role: 'Andriod Mentor', complexion: 'Dark'}
    ],
    text: 'I am learning more about view'
   }
  },
  methods: {
    increseCount() {
      this.count++;
      if (this.count == 10) {
        document.querySelector(".hello").classList.add("purple");
        document.querySelector(".hello").classList.remove("green");
      }else{
        document.querySelector(".hello").classList.remove("green");
      }
    },
  }
}
</script>

<style scoped>
.card-holder{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 20px;
}  
.card{
  height: 15em;
  width: 20%;
  border: 1px solid hsl(0, 0%, 0%);
  border-radius: 12px;
  text-align: center;
  background-color: rgb(146, 197, 197);
  padding: 50px;
}
.text{
  font-family: sans-serif;
  font-size: 17px;
  text-transform: capitalize;
  padding-bottom: 10px;
}
.sec{
  margin-top: 40px;
}
.purple{
  background: #800080;
  color: #fff;
}
.green{
  background: #1efd00;
  color: #fff;
}
</style>

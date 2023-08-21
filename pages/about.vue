<template>
    <div>
      <img :src="picture" :width="size" :height="size">
      <p>ชื่อ :{{ firstname }}</p>
      <p>นามสกุล :{{ lastname }}</p>
      <p>อายุ :{{ age }}</p>
      <p>ที่อยู่ :<span v-html="address"></span></p>
      <p v-if="hobby.length ===0">ไม่มีงานอดิเรก</p>
      <p v-else>งานอดิเรก :</p>
        <ul>
            <li v-for="item in hobby">{{ item }}</li>
        </ul>
      <p>ข้อมูลพื้นฐาน : </p>
        <ul>
          <li v-for="(value,key) in general" :key="key" > {{ key }} : {{ value }}</li>
        </ul>    
        <button @click="showData">คลิกเพื่อดูข้อมูล</button>
        <button @click="increment">เพิ่มเติมค่า</button>
        <button @click="decrement">ลดค่า</button> 
    </div>
  </template>
  <script>
    export default{
      data(){
        return{
          firstname: "Ratchanon",
          lastname: "Pakdee",
          age: 18,
          address: "<i>Chonburi</i>",
          picture: "https://rms.tatc.ac.th/files/importpicstd/01/66309010014.jpg",
          size: 250,
          hobby : ["-เล่นเกม","-ดูหนัง","-ฟังเพลง"],
          general : {gender:"Man",weight:46,height:170,status:false},

          methods :{
            getFullname(){
                return `$(this.firstname) $(this.lastname)`
            },
            showData(){
                alert(this.firstname)
            },
            increment(value){
                this.age += value
            },
            decrement(value){
                this.age -= value
            },
            setNickname(event){
                this.nickname=event.target.value
            },
            submidForm(e){
                e.preventDefault();
                alert('บันทุกข้อมูลเรียบร้อย')
            }
        }
        }
      }
    }</script>
<template>
    
    
        <body class="tbody">
<div class="kotakk">
                Irvanda Ibrahim profile
</div>
        <section>
            
            
          <nav class="navv">
        
                  <div v-for="mn in cv2" :key="mn" >  
                <br>
                <br> 
                <img src="https://mipa.unnes.ac.id/ssc/wp-content/uploads/2017/02/PngItem_4196791-1063x1080.png" height="145" width="150" style="pading: right 100px" >
            <hr style="2px">
             <h3 class="h3">
                PROFILE <hr class="hr">
            </h3>
            <h4 class="h4"> NAME 
                <h5 class="h5">{{mn.nm}}</h5>
            
            <br>
            DATE OH BIRTH
                <h5 class="h5">{{mn.ttl}}</h5>
            <br>
            ADDRESS 
            <h5 class="h5"> {{mn.almt}} </h5>
            <br>
            ✉️ WEBSITE
            <h5 class="h5"> <a href="https://mail.google.com/mail/u/0/?tab=rm&ogbl">{{mn.web}}</a></h5>
            <br>
            
            <br>
            <hr class="hr">
            <h3>CONTACT</h3>☎️
            Home Number
            <h5 class="h5">{{mn.hn}}</h5>
            <h5 class="h5">My:              <a href="https://wa.me/qr/7YTMT33D2PUUH1">WhatsApp</a></h5>
            <br>
            <hr class="hr">
            Social Media:
            <h5 class="h5">IG: <a href="https://www.instagram.com/irvanda_ibra?r=nametag">{{mn.ig}}</a></h5>
            <h5 class="h5">FB: <a href="https://www.facebook.com/irvanda.ibrahim">{{mn.fb}}</a></h5>
            <br>
            <br>
            </h4>
                  </div>
        
          </nav>
          
          <article class="article">
              <div v-for="mn in cv2" :key="mn">
              <br>
              <br>
            <div class="kotak"> 

                <h3>💼PENGALAMAN KERJA</h3><hr class="hrr">
                <br>
                    <h4>belum bekerja</h4>

            </div>
            <br>
            <br>
            <br>
            <br>
            <div class="kotak">
                <h3>🏫PENDIDIKAN</h3>
                    <hr class="hrr">
                    <li>TK</li>
                    <li>SD</li>
                    <li>SMP</li>
                    <lI>SMK</lI>
            </div>
            <br>
            <br>
            <br>
            <br>
                <div class="kotak">
                    <h3>💻KEMAMPUAN</h3>
                    <hr class="hrr">
                    <h4>Microsoft &#9899; &#9899; &#9899; &#9899; <span style="color: black; opacity 50%">&#9899; </span></h4>
                    <h4>hTML &#9899; &#9899; &#9899; &#9899; &#9899;</h4>
                    <h4>CSS &#9899; &#9899; &#9899; &#9899; &#9899;</h4>
                    <h4>JavaScript &#9899; &#9899; &#9899; &#9899; </h4>
                </div>
            </div>
          </article>
          
        </section>
        
        </body>

</template>

<script>
/* eslint-disable */ 
export default {
    name: 'CvDua'
};
</script>
<script>
import axios from 'axios'
export default {
    data(){
        return{
            cv2: []
        }
    },

  mounted() {
    this.load()
  },
  methods: {
    load(){
        axios.get('http://localhost:3000/cv2').then(res => {
        this.cv2 = res.data //respon dari rest api dimasukan ke users
      }).catch ((err) => {
        console.log(err);
      })
    }
   }
  }
</script>
<style>
.tbody {
  background-color: rgb(255, 255, 255);
}


* {
    box-sizing: border-box;
  }
  .hr {
      border: 1px dashed black;
      opacity: 60%;
  }
  
  body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 100px;
  }
  
  section {
    display: -webkit-flex;
    display: flex;
  }
  
  .navv {
      border: 1px solid rgb(214, 214, 214); 
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    background: #ffff;
    padding: 40px;
    text-align: left;
  }

  #nama {
      font-family: Verdana;
      font-size: 25px;
      color: black;
      opacity: 50%;
  }

  h2 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    opacity: 75%;
  }

  .kotakk {
      text-align: left;
      font-family: cursive;
      font-size: 20px;
      padding: 10px;
      color: rgb(255, 255, 255);
      border: none;
      width: 827px;
      height: 100px;
      background-color: rgb(13, 13, 90);
  }

  .article {
    -webkit-flex: 3;
    -ms-flex: 3;
    flex: 3;
    background-color: rgb(240, 240, 240);
    padding:40px;
    text-align: center;
    border: 1px solid rgb(214, 214, 214);
  }
  
  #p1 {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    opacity: 75%;
  }
  #p2{
    font-family: Georgia, 'Times New Roman', Times, serif;
    opacity: 85%;
  }

  .kotak {
      text-align: none;
      border-radius: 5px;
      background-color: #e9e9e9;
      padding: 10px;
      margin: auto;
      opacity: 60;
  }

  @media (max-width: 600px) {
    section {
      -webkit-flex-direction: column;
      flex-direction: column;
    }
  }

  .h3 {
    opacity: 95%;
    text-align: right;
  }
  .h5 {
    opacity: 90%;
    text-align: right;
  }
  .h4 {
      text-align: right ;
  }
  .hrr {
    border: 2px solid black;
  }
</style>



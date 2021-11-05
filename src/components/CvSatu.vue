<template>
   
        <body class="tbody">

        <section>
          <nav>
            <div v-for="nm in cv1" :key="nm.id">
            <div id="nama">
              {{nm.nama}}
                <font style="color: rgb(102, 121, 129)">{{ nm.nama1 }}</font>
            </div>
                <br>
                <br> 
                <img src="WhatsApp Image 2021-11-04 at 10.39.43.jpeg" height="300" width="200" >
            
            <h3>
                Contact <hr>
            </h3>
            <h5 id="o2">Address:
                <p> {{nm.alamat}} </p>
            
            <br>
            Phone:
                <p>{{nm.no}}</p>
            <br>
            Email:
                <p><a href="">{{nm.email}} </a></p>
            <br>
            Social Media:
            <p>IG: <a href="https://www.instagram.com/irvanda_ibra?r=nametag">{{nm.ig}}</a></p>
            <p>FB: <a href="https://www.facebook.com/irvanda.ibrahim">{{nm.fb}}</a></p>
            <br>
            <br>

            <h3>Languages</h3><hr>
            <br>
            {{nm.bhs}}
            <br>
            {{bhs2}}
            <br>
            <br>

            <h3>Hobbies</h3><hr>
            
            <ul>
                <li>{{nm.hobi1}}</li>
                <li>{{nm.hobi2}}</li>
                <li>{{nm.hobi3}}</li>
                <li></li>
              </ul>  
            </h5>
            </div>
          </nav>
          
          <article>
              <div v-for="nm in cv1" :key="nm">
            <h2>
                Inilah Aku<hr>
            </h2>
            <p id="p1">
                {{nm.r}}
            </p>
            <br>
            <br>
            <p id="p1">
                <h2>Skill Highlights</h2><hr>
                <ul id="p1">
                    <li>{{nm.s}}</li>
                    <li>{{nm.s2}}</li>
                    <li>{{nm.s3}}</li>
                    <li>{{nm.s4}}</li>
                    <li>{{nm.s5}}</li>
                </ul>
            
            <br>
            <br>
            <p>
                <h2>Experience</h2><hr>       
                <p id="p2">{{nm.ex}}</p>
                <ul id="p1">
                    <li>{{nm.ex1}}</li><br>
                     <li>{{nm.ex2}}</li><br>
                    <li>{{nm.ex3}}</li><br>
                </ul> 
            
            <br>
            <br>

            <p>
                <h2>Education</h2><hr>
                <p>-</p>
            
            <br>
            <br>
            <p>
                <h2>Certifications</h2><hr>
                <p id="p1">{{nm.ser}}</p>
            </div>
          </article>
        </section>
        
        </body>

</template>

<script>
/* eslint-disable */ 
export default {
    name: 'CvSatu'
};
</script>
<script>
import axios from 'axios'
export default {
    data(){
        return{
            cv1: []
        }
    },

  mounted() {
    this.load()
  },
  methods: {
    load(){
        axios.get('http://localhost:3000/cv1').then(res => {
        this.cv1 = res.data //respon dari rest api dimasukan ke users
      }).catch ((err) => {
        console.log(err);
      })
    }
   }
  }
</script>
<style>
.tbody {
  background-color: gray;
}



* {
    box-sizing: border-box;
  }
  
  body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 100px;
  }
  
  section {
    display: -webkit-flex;
    display: flex;
  }
  
  nav {
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    background: #ccc;
    padding: 40px;
  }

  #nama {
      font-family: Verdana;
      font-size: 25px;
      color: black;
      opacity: 80%;
  }

  h2 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    opacity: 75%;
  }

  article {
    -webkit-flex: 3;
    -ms-flex: 3;
    flex: 3;
    background-color: #f1f1f1;
    padding:40px;
  }
  
  #p1 {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    opacity: 85%;
  }
  #p2{
    font-family: Georgia, 'Times New Roman', Times, serif;
    opacity: 85%;
  }

  @media (max-width: 600px) {
    section {
      -webkit-flex-direction: column;
      flex-direction: column;
    }
  }

  h3 {
    opacity: 95%;
  }
  h5 {
    opacity: 90%;
  }
</style>
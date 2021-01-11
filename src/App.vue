<template>
  <body>

    <div class="wrap">
      <div class="top">
        <div class="navbar">
          <a href="https://www.nba.com/" class='nbaLogo'>
            <img src="https://cdn.nba.com/logos/leagues/logo-nba.svg" alt="">
            <!-- <span>NBA</span> -->
          </a>
          <ul class="navbar-menu">
            <a href="#"><li @mouseover="sayhi()">Games</li></a>
            <a href="#"><li>Schedule</li></a>
            <a href="#"><li>Watch</li></a>
            <a href="#"><li>News</li></a>
            <a href="#"><li>Standings</li></a>
            <a href="#"><li>Teams</li></a>
            <a href="#"><li>Stats</li></a>
            <a href="#"><li>Players</li></a>
            <a href="#"><li>Fantasy</li></a>
            <a href="#"><li>NBA Official</li></a>
            <a href="#"><li class="nbatv">NBA TV</li></a>
            <a href="#"><li>League Pass</li></a>
            <a href="#"><li>Store</li></a>
            <a href="#"><li>Tickets</li></a>
            <a href="#"><li>Others</li></a>
            <a href="#"><li>Sign In</li></a>
            
          </ul>

        </div>

        <div class="scoreboard">
          <ul>
            <li>Date</li>
            <li>PHI x BKN</li>
            <li>CLE x MEM</li>
            <li>DAL x DEN</li>
            <li>SAS x LAL</li>
            <li>MIN x POR</li>
            <li>I'm ignoring</li>
          </ul>

        </div>
      </div>


      <div class="main">

        <div class="herobox">

          <div class='hero-top'>
            <div class="pic4" v-if="heromenu === 1">
              <div class="hero-caption">
                <strong>Pistons Host Jazz To Begin 8-Game Sunday</strong>
                <button>BOX SCORE</button>
              </div>
              <img src="https://cdn.nba.com/manage/2021/01/mitchell-layup-pistons-scaled-e1610309855200.jpg" alt="" class="menuPic">
            </div>
            <div class="pic4" v-if="heromenu === 2">
              <div class="hero-caption">
                <strong>Bulls Face Off Against Clippers in L.A.</strong>
                <button>BOX SCORE</button>
              </div>
              <img src="https://cdn.nba.com/manage/2021/01/coby-white-clippers-scaled-e1610314854417.jpg" alt="" class="menuPic">
            </div>
            <div class="pic4" v-if="heromenu === 3">
              <div class="hero-caption">
                <strong>Durant Returns To The Floor Against Thunder</strong>
                <button>BOX SCORE</button>
              </div>
              <img src="https://cdn.nba.com/manage/2021/01/GettyImages-1230384731-scaled-e1610311887270.jpg" alt="" class="menuPic">
            </div>
            <div class="pic4" v-if="heromenu === 4">
              <div class="hero-caption">
                <strong>Kia MVP Ladder: LeBron Starts Chase on Top</strong>
                <span>The Lakers' star holds NO.1 spot in Sekou Smith's first ranking of Kia MVP</span>
                <button>READ</button>
              </div>
              <img src="https://cdn.nba.com/manage/2021/01/lebron-davis-high-five-scaled-e1610305291505.jpg" alt="" class="menuPic">
            </div>
            <div class="pic4" v-if="heromenu === 5">
              <div class="hero-caption">
                <strong>Lamelo Ball Youngest Ever To Post Triple-Double</strong>
                <span>The 19-year-old guard set the record with 22 points, 12 rebounds and 11 assists in a win over Atlanta</span>
                <button>READ</button>
              </div>
              <img src="https://cdn.nba.com/manage/2021/01/20210109_LAMELO_DRIBBLE-e1610253094483.jpg" alt="" class="menuPic">
            </div>
          </div>


          <div class="hero-menu">
            <div class="hero-menu1 down-menu" @click="changeHero(1)" :class="[heromenu === 1 ? 'nopa': 'opa']" >
              <small>ON NBA TV</small>
              <span>Pistons Host Jazz To Begin 8-Game Sunday</span>
              
            </div>
            <div class="hero-menu2 down-menu" @click="changeHero(2)" :class="[heromenu === 2 ? 'nopa': 'opa']">
              <small>ON LEAGUE PASS</small>
              <span>Bulls Face Off Against Clippers in L.A.</span>
            </div>

            <div class="hero-menu3 down-menu" @click="changeHero(3)" :class="[heromenu === 3 ? 'nopa': 'opa']">
              <small>ON LEAGUE PASS</small>
              <span>Durant Returns To The Floor Against Thunder</span>
            </div>

            <div class="hero-menu4 down-menu" @click="changeHero(4)" :class="[heromenu === 4 ? 'nopa': 'opa']">
              <small>Feature</small>
              <span>Kia MVP Ladder: LeBron Starts Chase on Top</span>
            </div>

            <div class="hero-menu5 down-menu" @click="changeHero(5)" :class="[heromenu === 5 ? 'nopa': 'opa']">
              <small>NEWS</small>
              <span>Lamelo Ball Youngest Ever To Post Triple-Double</span>
            </div>
          </div>
          
        </div>
        <div class="main-leftside"></div>
        <div class="main-rightside"></div>
      </div>
    </div>
    
  </body>
  
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      heromenu:  1,
    }
  },

  methods:{
    changeHero(num){
      this.heromenu = num;
    }  
  }
}


</script>

<style>
body {
margin:0;
padding:0;
}

.navbar{
  background-color: rgba(5,28,45);
  width: 100%;
  height: 50px;
  position: absolute;
}
.nbaLogo{
  margin-left: 320px;
  margin-top: 2px;
  position: absolute;
  width: 80px;
  height: 80px;
}
.nbaLogo img{
  width: 45px;
  height: 45px;
}
.navbar a:link,
.navbar a:visited,
.navbar a:hover,
.navbar a:active{
  text-decoration: none;
  color: white;
}
.navbar-menu{
  margin-top: 16px;
  margin-left: 350px;
  font-size: 100%;
  display: flex;
  color: white;
  list-style: none;
}
.navbar-menu li{
  margin-right: 15px;
}
.nbatv{
  margin-left: 200px;
}


.scoreboard{
  background-color:red;
  width: 100%;
  height: 75px;
  position: absolute;
  top: 50px;

  box-shadow: 0px 15px 10px -15px #111; 
}
.scoreboard ul{
  
  /* position: absolute; */
  /* top: -20; */
  border: solid black 1px;
  /* padding-top: -50px; */
  /* padding: 30px; */
  /* padding-bottom: 50px; */

}
.scoreboard li{
  width: 75px;
  display: inline;
  margin-right: 2.5px;
  margin-left: 10px;
  /* padding-top: 15px;
  padding-bottom: 15px; */

  display: inline-block;
  vertical-align: top;
  overflow-y: hidden;
  max-height: 90px;

  flex-direction: column;
  border-right-width: 1px;
  --border-opacity: 1;
  border-color: black;
  padding: 0.5rem;

  /* border: solid white 1px; */

  
  /* margin-top: 100px */
}
.separationLine{
  margin-top: -30px;
  color: blue;
  font-size: 100px;
  top: 50px;
}




.herobox{
  background-color:black;
  width: 100%;
  height: 550px;
  position: absolute;
  top: 150px;
}

.hero-caption{
  /* background-color:yellow; */
  width: 40%;
  height: 300px;
  position: absolute;
  top: 100px;
  margin-left: 30px;
  color: white;
}

.hero-top strong{
  /* position: absolute; */
  left: 50px;
  height: 100px;
  font-size: 300%;
}

.hero-top span{
  
  position: absolute;
  margin-top: 30px;
}

.hero-top button{
  color: white;
  position: absolute;
  margin-top: 70px;
  background-color: black;
  padding: 10px;
      padding-left: 2rem;
    padding-right: 2rem;

  border-radius: 9999px;
  border-width: 2px;
  --border-opacity: 1;
      border-color: rgba(255,255,255,var(--border-opacity));
}

.hero-top strong:after {
  content:"\a";
  white-space: pre;
}

.menuPic{
  position: absolute;
  width: 680px;
  height: 400px;
  box-shadow: 0 0 8px 8px black inset;
  right: 0;
}

.hero-menu{
  display: flex;
  bottom: 0;
  position: absolute;
  bottom: 10px;
  
  /* opacity: 0.3; */
}

.opa{
  opacity: 0.3;
  animation-duration: 3s;
}

.nopa{
  
}

.down-menu{
  
  color: white;
  margin-right: 50px;
  cursor: pointer;
}

.down-menu:nth-of-type(1){
  margin-left: 50px;
}

.down-menu small:after {
  content:"\a";
  white-space: pre;
}

</style>

<template>

  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  </head>
 
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


        <div class="main-leftside">


          <div class="section-playWeek">
            <strong class="boxTitle">PLAYER OF THE WEEK</strong>
            <small>See more</small>
            <hr class="hrLine">
            <div class="group-of-clips">
              <div class="weeklyClip">
                <iframe src="https://www.youtube.com/embed/SPcYVUn5TbQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <span class="video-caption">Week 1 Top Plays</span>
              </div>

              <div class="weeklyClip">
               <iframe src="https://www.youtube.com/embed/B4wANmb8ICQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <span class="video-caption">Week 2 Top Plays</span>
              </div>

              <div class="weeklyClip">
                <iframe src="https://www.youtube.com/embed/Yz2QqJ9UnK8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <span class="video-caption">Week 3 Top Plays</span>
              </div>
            </div>
          </div>
          <div class="section-coivd19">
            <div class="covid-top">
                <strong class="boxTitle">COVID-19 NBA NEWS</strong>
              <hr class="hrLine">
            </div>
            <div class="covid-bottom">
              <div class="covid-left">
                <img src="https://cdn.nba.com/manage/2021/01/GettyImages-1230525513-scaled-e1610481249831.jpg" alt="">
                <strong class="covid-main-title">NBA, NBPA agree to additional measures to supplement Health and Safety protocols</strong>
                <small>New measures include Players wearing on the bench at all times</small>
              </div>
              <div class="covid-right">
                <div class="covid-articles-group">
                  <span>Jazz-Wizards game postponed for Health and Safety Protocols</span>
                  <hr>
                  <span>Magic-Celtics game postponed due to Health and Safety Protocol</span>
                  <hr>
                  <span>Wizards opt to cancel practice Tuesday</span>
                  <hr>
                  <span>Monty Williams shares perspective on teams' safety
</span>
                  <hr>
                  <span>New Orleans vs. Dallas, Boston vs. Chicago games postponed</span>
                  <hr>
                  <span>Hawks to allow ticketed fans to games starting Jan. 26</span>
                  <hr>
                  <span>Heat-Celtics game postponed due to Health and Safety Protocols</span>
                  <hr>
                </div>

              </div>
            </div>
            
            
          </div>
          <div class="section-analysis">
            <strong class="boxTitle">ANALYSIS</strong>
            <hr class="hrLine">
            <div class="analysis-both-sides">
                <div class="analysis-left">

                  <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/chris-paul-iso-smile-scaled-e1610383963740.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                        <strong>Power Rankings, Week 4: Suns rise to No. 2; Warriors move into Top 10
                        </strong>
                      <small>See how all 30 teams rank after the first three weeks of the 2020-21 season.
                      </small>
                      <span>January 11, 2021</span>
                    </div>
                  </div>

                  <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/carmelo-lebron-iso.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                      <strong>10 facts to know from the 2020-21 NBA Roster Survey</strong>
                      <small>Interesting facts abound in the NBA's annual look at the opening-night rosters for all 30 teams</small>
                      <span>January 7, 2021</span>
                    </div>
                  </div>

                  <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/pete-maravich-iso-looks-iso.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                      <strong>The final day of 'Pistol Pete' Maravich</strong>
                      <small>The Hall of Famer died suddenly and unexpectedly in 1988 at 40.
                      </small>
                      <span>January 6, 2021</span>
                    </div>
                  </div>

                </div>
              <div class="analysis-right">

                <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/lamelo-ball-looks.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                        <strong>Kia Rookie Ladder: LaMelo Ball holds No. 1 spot after first three weeks
                        </strong>
                      <small>The Hornets' rookie starts on top in the first ranking of 2020 NBA Draft class.
                      </small>
                      <span>January 11, 2021</span>
                    </div>
                  </div>

                  <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/sabonis-reacts-e1610466810112.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                      <strong>10 facts to know from the 2020-21 NBA Roster Survey</strong>
                      <small>Pacers' All-Star Domantas Sabonis reaching new levels this season
                      The skilled big man has dominated during the first 10 games after missing the entire 2019-20 season restart in Orlando.
                      </small>
                      <span>January 7, 2021</span>
                    </div>
                  </div>

                  <div class="analysis-article">
                    <img src="https://cdn.nba.com/manage/2021/01/lebron-looks-isos.jpg?w=384&h=224" alt="">
                    <div class="analysis-article-right-side">
                      <strong>Kia MVP Ladder: LeBron James starts at the top as new chase begins
                      </strong>
                      <small>The Lakers' star holds the No. 1 spot in Sekou Smith's first ranking of Kia MVP candidates.
                      </small>
                      <span>January 6, 2021</span>
                    </div>
                  </div>

              </div>
            </div>
            
          </div>

          <!-- <div class="section-video-boxscores"></div>
          <div class="section-features"></div>
          <div class="section-inside"></div>
          <div class="section-hangtime"></div>
          <div class="section milestones"></div> -->
        </div>

        <div class="main-rightside">
          <div class="section-standings">
            <div class="standing-top">
              <span>2020-21 Sandings</span>
              <small>Go to Settings</small>
              <button class="btn-east">EASTERN</button>
              <button class="btn-west">WESTERN</button>

            </div>
            <div class="standing-bottom"></div>
          </div>
          <div class="section-leaders"></div>
          <div class="section-followNBA"></div>
          <div class="section-links"></div>
          <div class="section-email"></div>
        </div>

        
      </div>

      <div class="bottom-copyright">
        <div class="copy-top">
          <div class="copy-col">
            <strong>NBA ORGANIZATION</strong>
            <span>NBA OFficial</span>
            <span>NBA Careers</span>
          </div>

          <div class="copy-col">
            <strong>NBA INTIATIVES</strong>
            <span>NBA Cares</span>
            <span>Jr.NBA</span>
            <span>NBA Voices</span>
            <span>NBA Fit</span>
            <span>Hoops for Troops</span>
          </div>

          <div class="copy-col"> 
            <strong>ACROSS THE LEAGUE</strong>
            <span>NBA Communications</span>
            <span>Lockervision</span>
            <span>NBA Transactions</span>
          </div>

          <div class="copy-col copy-shop">
            <strong>SHOP</strong>
            <span>Global Stores</span>
            <span>NYC Stores</span>
            <span>NBA Auctions</span>
            <span>NBA Photostore</span>
          </div>


          <div class="copy-col">
            <strong>SUBSCRIPTION</strong>
            <span>NBA TV</span>
            <span>League Pass</span>
          </div>
        </div>
        <hr class="hrLine">
        <div class="copy-bottom">
          <small>© 2021 NBA Media Ventures, LLC. All rights reserved.</small>
        </div>

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
background-color: #E8E8E8;
}

.boxTitle{
  position: absolute;
  margin-left: 30px;
  margin-top: 13px;
}

.hrLine{
  width: 90%;
  border: 0;
  border-top: 1px solid grey;
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



.main-leftside{
  
  /* border: solid black 1px; */
  width: 60%;
  height: 2750px;
  top: 720px;
  position: absolute;
  color: white;
  left:5%;
}



.section-playWeek{
  background-color: white;
  width: 100%;
  height: 275px;
  top: 0px;
  position: absolute;
  color: black;
}
.section-playWeek small{
  margin-top: 15px;
  right: 30px;
  position: absolute;
  color: DodgerBlue;
}
.section-playWeek hr{
  margin-top: 40px;
}
.group-of-clips{
  margin-left: 25px;
  display: flex;
  margin-top: 20px;
}
.weeklyClip{
  /* border: solid black 1px; */
  margin-left: 30px;
  display: flex;
  width: 270px;
}
.section-playWeek iframe{
  width: 250px;
  height: 150px;
}
.video-caption{
  position: absolute;
  color:  black;  
  margin-top: 170px;
  margin-left: 65px;
}




.section-coivd19{
  background-color: white;
  width: 100%;
  height: 500px;
  top: 300px;
  position: absolute;
  color: black;
}
.covid-top{
  width: 100%;
  height: 10%;
  top: 0px;
  position: absolute;
  color: black;
}
.covid-top hr{
  margin-top: 40px;
}
.covid-bottom{
  width: 100%;
  height: 90%;
  top: 10%;
  position: absolute;
  color: black;
}
.covid-left{
  width: 60%;
  height: 100%;
  top: 0px;
  position: absolute;
  color: black;
}
.covid-left img{
  margin-top: 10px;
  margin-left: 30px;
  width: 500px;
  height: 300px;
}
.covid-main-title{
  position: absolute;
  left: 30px;
  top: 320px;
  font-size: 150%;
}
.covid-left small{
  position: absolute;
  left: 30px;
  top: 390px;
  font-size: 100%;
}
.covid-right{
  /* background-color: red; */
  width: 35%;
  height: 100%;
  top: 0px;
  left: 60%;
  position: absolute;
  color: black;
}
.covid-articles-group{
  margin-top: 40px
}





.section-analysis{
  /* background-color: white; */
  width: 100%;
  height: 450px;
  top: 830px;
  position: absolute;
  color: black;
}
.section-analysis hr{
  margin-top: 40px;
}

.analysis-both-sides{
  margin-top: 20px;
}


.analysis-left{
  /* background-color: grey; */
  width: 47.5%;
  height: 90%;
  top: 10%;
  position: absolute;
  color: black;
}

.analysis-article{
  background-color: white;
  margin-bottom: 24px;
  height: 30%;
}

.analysis-article img{
  width: auto;
  height: 100%;
}

.analysis-article-right-side{
  position: absolute;
  left: 45%;
  width: 55%;
  margin-top: -120px;
}

.analysis-article-right-side strong:after,
.analysis-article-right-side small:after {
  content:"\a";
  white-space: pre;
}






.analysis-right{
  /* background-color: blue; */
  width: 47.5%;
  left: 52.5%;
  height: 90%;
  top: 10%;
  position: absolute;
  color: black;
}






.main-rightside{
  background-color: white;
  border: solid black 1px;
  width: 28%;
  height: 275px;
  top: 720px;
  position: absolute;
  color: white;
  right:5%;
}









.bottom-copyright{
  background-color: rgba(5,28,45);
  width: 100%;
  height: 275px;
  top: 2500px;
  position: absolute;
  color: white;
}
.copy-top{
  display: flex;
  margin-top: 35px;
  margin-bottom: 35px;
}
.copy-top span{
  cursor: pointer;
  display: flex;
  margin-top: 10px;
  font-size: 75%;

}
.copy-col{

  margin-left: 100px;
}
.copy-shop{
  margin-top: 10px;
  margin-right: 300px;
}
.bottom-copyright small{
  margin-top: 10px;
  position: absolute;
  left: 100px;
}



</style>

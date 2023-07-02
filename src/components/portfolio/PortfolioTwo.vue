<template>
  <div>
  <div class="container">
    <div
      class="positon-relative"
     
    >
      <div class="shane_tm_title">
        <div class="title_flex">
          <div class="left">
            <span>Portfolio</span>
            
          </div>
        </div>
      </div>

  
      <!-- End shane_tm_title -->
      <div class="portfolio_filter">
        <ul>
          <li>
            <a
              v-on:click="activetab = 1"
              :class="[activetab === 1 ? 'active' : '']"
              >UX Projects</a
            >
          </li>
          <!-- End All for tabcontent 1 -->
          <li>
            <a
              v-on:click="activetab = 2"
              :class="[activetab === 2 ? 'active' : '']"
              >AR/XR</a
            >
          </li>
          <!-- End AR/VR tabcontent 2 -->
          <li>
            <a
              v-on:click="activetab = 3"
              :class="[activetab === 3 ? 'active' : '']"
              >Design</a
            >
          </li>
          <!-- End .Youtube tabcontent 3 -->
          <li>
            <a
              v-on:click="activetab = 4"
              :class="[activetab === 4 ? 'active' : '']"
              >3D</a
            >
          </li>
          <!-- End Mix tabcontent 4 -->
        </ul>
      </div>
      <br>
      <!-- End .portfolio-filter -->
    </div>

    <div v-if="activetab === 1" class="tabcontent">
      <div class="portfolio_list">
        <ul >
          <!-- <CoolLightBox :items="uxItems" :index="index" @close="index = null">
          </CoolLightBox> -->

<!-- ___________________________ posts UX projects ______________________________-->
          <li style="padding-left: 7%;">
            <div class="inner" @click="showModal1">
              <div class="">
                <img class="image" src="../../assets/img/_/AR/Food4Me.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                             <img src="../../assets/img/_/project3.png" alt="Play Icon">
                      </div>
           </div>
              
                <div  style="color: black; 
                text-align: center;  justify-content: center; align-items: center;"
                  >
                  <div id="ar-xr-tab" class="custom-post-title">UX Project - App (Food4me)</div>
                  <div>to achieve long-term healthy nutrition</div></div>
   
          </li>

          <li style="padding-left: 7%;">
            <div class="inner" @click="showModal2">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/AR/virtualGarden.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
             <div class="mobile_title">
                           <img src="../../assets/img/_/project3.png" alt="Play Icon">
                    </div>

                      </div>
                  <div  style="color: black; 
                  text-align: center;  justify-content: center; align-items: center;"
                    >
                    <div class="custom-post-title">UX Project - App (virtual Garden)</div>
                    <div>to understand the impact on climate change of personal behaviour <br>and help to improve it</div></div>
        
          </li>

          <li style="padding-left: 7%;">
            <div class="inner" @click="showModal3">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/ux/Tattoo App - Empathy Map.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                           <img src="../../assets/img/_/project3.png" alt="Play Icon">
                    </div>
   </div>
                  
                  <div  style="color: black; 
                  text-align: center;  justify-content: center; align-items: center;"
                    >
                    <div class="custom-post-title">UX Project - App (Tattoo)</div>
                    <div>to find the right tattoo artist and easily manage everything</div></div>
           
          </li>

          <li style="padding-left: 7%;">
            <div class="inner" @click="showModal4">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/AR/ARestaurant.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                         <img src="../../assets/img/_/project3.png" alt="Play Icon">
                  </div>
                     </div>
                  <div  style="color: black; 
                  text-align: center;  justify-content: center; align-items: center;"
                    >
                    <div class="custom-post-title">UX Project - App (ARestaurant)</div>
                    <div>to make the right meal decision that leaves you satisfied</div></div>

          </li>

          <!-- <li v-for="(image, imageIndex) in uxItems" :key="imageIndex">
            <div class="inner" @click="showModal1">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
             
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li> -->


          <!-- End li -->
        </ul>
      </div>

      <!-- End .portfolio_list -->
    </div>
    <!-- End .tabcontent 1 -->

    <div v-if="activetab === 2" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="arVrItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>
          <li  v-for="(image, imageIndex) in arVrItems" :key="imageIndex" style="padding-left: 7%;">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                 <img class="image" :src="image.thumb" alt="Portfolio" />
               
              </div>
              <!-- End           <video @loadedmetadata="playVideo" style="height:300px;" :src="image.src" muted loop></video>
              
              <h3>{{ image.portfolioName }}</h3>
              <span>{{ image.portfolioType }}</span>
                
                .entry -->
               <div class="mobile_title">
                       <img src="../../assets/img/_/play.png" alt="Play Icon">
                </div>

              
            </div> 
            <div v-if="image.portfolioName" class="custom-post-title"> {{ image.portfolioName }}</div>
            <div style="color: black; text-align: center; display: flex; justify-content: center; align-items: center;" v-if="image.details"> {{ image.details }}</div>
            <div style="color: orange; font-weight: bold; text-align: center; display: flex; justify-content: center; align-items: center;" v-if="image.additional"> {{ image.additional }}</div>

            <div style="text-align: center; display: flex; justify-content: center; align-items: center; margin-top: 25px;">
            <div v-if="image.buttn1" class="shane_tm_button">
              <a :href=image.buttn1url >{{ image.buttn1 }}</a></div>
            <div v-if="image.buttn2" class="shane_tm_button">
              <a :href=image.buttn2url >{{ image.buttn2 }}</a></div>
            <div v-if="image.buttn3" class="shane_tm_button">
              <a :href=image.buttn3url >{{ image.buttn3 }}</a></div>
            </div>

            <button href="" style="visibility: hidden;"></button>
          </li>
          <!-- btn-outline dreht um?- -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 2 -->

    <div v-if="activetab === 3" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="designItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>

            <li>
              <div class="inner" @click="showModal5">
                <div class="entry shane_tm_portfolio_animation_wrap">
                  <img class="image" src="../../assets/img/_/Design/magazin.png" alt="Portfolio" />
                </div>
                <!-- End .entry -->
                <div class="mobile_title">
                           <img src="../../assets/img/_/project3.png" alt="Play Icon">
                    </div>
              </div>

              <div  style="color: black; 
              text-align: center;  justify-content: center; align-items: center;"
                >
                <div class="custom-post-title">Magazine Design</div>
                <div>made in Indesign. with Photoshop and Illustrator.</div></div>



            </li>

          <li v-for="(image, imageIndex) in designItems" :key="imageIndex" style="padding-left: 7%;">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->

              <div  v-if="image.autoplay" class="mobile_title">
                                 <img src="../../assets/img/_/play.png" alt="Play Icon">
                          </div>
                          </div>

              <div v-if="image.portfolioName" class="custom-post-title"> {{ image.portfolioName }}</div>
              <div style="color: black; text-align: center; display: flex; justify-content: center; align-items: center;" v-if="image.details"> {{ image.details }}</div>
             
           
          </li>
          <!-- End li -->
        

        </ul>

        
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 3 -->

    <div v-if="activetab === 4" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="dreiDItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>

          <li v-for="(image, imageIndex) in dreiDItems" :key="imageIndex" style="padding-left: 7%;">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>

              <div v-if="image.autoplay" class="mobile_title">
                         <img src="../../assets/img/_/play.png" alt="Play Icon">
                  </div>

              
              </div> 
              <div v-if="image.portfolioName" class="custom-post-title"> {{ image.portfolioName }}</div>
              <div style="color: black; text-align: center; display: flex; justify-content: center; align-items: center;" v-if="image.details"> {{ image.details }}</div>
              <div style="color: orange; font-weight: bold; text-align: center; display: flex; justify-content: center; align-items: center;" v-if="image.additional"> {{ image.additional }}</div>

              <div style="text-align: center; display: flex; justify-content: center; align-items: center; margin-top: 25px;">
              <div v-if="image.buttn1" class="shane_tm_button">
                <a :href=image.buttn1url >{{ image.buttn1 }}</a></div>
              <div v-if="image.buttn2" class="shane_tm_button">
                <a :href=image.buttn2url >{{ image.buttn2 }}</a></div>
              <div v-if="image.buttn3" class="shane_tm_button">
                <a :href=image.buttn3url >{{ image.buttn3 }}</a></div>
                </div>
               
          </li>

         <!--    Modal für CAD erstmal weg. erst wenn ux & alles fertig wenn ich will nochmal an
            
          <li>
            <div class="inner" @click="showModal6">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/3D/catia_cad.png" alt="Portfolio" />
              </div>
             End .entry 
              <div class="mobile_title">
                             <img src="../../assets/img/_/project3.png" alt="Play Icon">
                      </div>
            </div>

            <div  style="color: black; 
                text-align: center;  justify-content: center; align-items: center;"
                  >
                  <div class="custom-post-title">CAD (Catiav5/Solidworks)</div>
                  <div>open to read details about my 3 years experience as cad product designer/konstrukteur.</div></div>

          </li> -->
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 4 -->

  </div>
  <div class="news_list">
    <ul>
<!------------------------------------------------------------------------------------------ food 4 me-->
      <li>
        <transition name="fade">
          <!-- Modal -->
          <div :class="{ 'modal-mask': isActive }" id="modal" @click="closeModal" v-if="isVisible">
            <div class="modal-dialog modal-dialog-centered " @click.stop>
              <div class="modal-content">
                <div class="close" @click="closeModal">
                  <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
                </div>
                <!-- End .close -->
                <div class="shane_tm_modalbox_news">
                  <div class="box_inner">
                    <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
                    <!-- End image -->
                    <div class="details">
                      <h3 class="title">
                        Food4me<img src="../../assets/img/_/icons/avocado.png" style="height:30px; margin-left: 1em;">
                      </h3>
                      <p class="date">
                        <a href="#"> </a>
                   
                      </p>
                    </div>
                    <!-- End details -->
   
                    </div>

                    

                    <div class="description" style="color: black; font-size: 1em;">

                      <p>This Project was my Bachelorthesis and about "creating a user-centered smartphone App for Nutrition".<br>
                      Below you see an Overview how my UX Process was structured.</p> 

<!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
  
                     
                      <img src="../../assets/img/_/text-info/food4me_info_green.png" style="display: block; margin: 0 auto; width: 90%;">
<!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
  <div class="description" style="color: black; font-size: 1.4em; text-decoration: underline; font-weight: bold;">Process</div>
                      <img src="../../assets/img/_/text-overview/overview_food4me.png" style="width: 40%">
                    <br>
                 
                    <br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                    

                      
                        <br>
                          <h6>
                            Secondary Research 
                          </h6><br>
                          <p>
                            As first step i did some research which results you can read detailed in my <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bachelorthesis</a>
                          </p>
                          <br>
                  
 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                    

                      
                      <br>
                        <h6>
                          Focusgruppe 
                        </h6><br>
                        <p>
                          Conducting a focus group allowed me to gather insights from potential users about their attitudes towards healthy eating and the challenges they face in maintaining a healthy diet in the long run. This information was used to inform the design of the app, ensuring that it meets the needs and expectations of its target audience. 
                        </p>
                        <br>
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>                  
                      
                        <br>
                          <h6>
                            User Story Map 
                          </h6><br>
                          <p>
                            Creating a user story map helped to identify the various user journeys and scenarios that the app needed to support, allowing me to design a seamless and intuitive user experience. This methodology allowed me to prioritize the features and functionality of the app based on user needs and ensure that the app supports long-term healthy eating habits. 
                          </p>
                          <br>
                  
               
                      
                    
                      <img src="../../assets/img/_/ux/Food4me - User Story Map.png" style="display: block; margin: 0 auto; width: 100%;">
                         <br>
                      <br>
 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                            <br><h6>
                              Use Case Diagram 
                            </h6><br>
                            <p>
                              Developing a use case diagram helped to visualize how the app would be used by different types of users, and the various interactions between them and the app. This diagram provided a clear overview of the app's functionality, allowing me to identify potential usability issues and design solutions that simplify the user experience. 
                            </p>
                            <br>

                         <img src="../../assets/img/_/ux/Food4me - Use Case Diagram.png" style="display: block; margin: 0 auto; width: 100%;">
   
                    <br>
                     <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                            <br><h6>
                          Brainstorming / Concept creation
                            </h6><br>

                            <p>After using some software design Methods (Usage requirements, functional requirements, non-functional requirements etc) at this point
                              , i created based on my findings of my Research a Concept. (for more details <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bachelthesis</a>)
                              To test and proof my findings i created two versions of paperprototyps, Later i compare and evaluate in an A/B Testing.
                              <br>
                       
                              For visualising purpose of Design and Navigation Brainstorming i created a <a href="https://miro.com/app/board/uXjVO84jJ7A=/" style="color:green">Miro Board</a>
                            </p>
                            <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
  <br><h6>
                            Paperprototyps
                              </h6><br>
                        
                              Following you can see my two Paperprototyps in a short description (more detailed here in <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bachelorthesis</a>)<br> <br>
                              <i style="font-weight: bolder; color: orange;">Paperprototyp 1</i> <br>
                              The Navigation is via Tabbar on the bottom.<br> <br> 
                              On the left Tab is the fuction for the use case "Buy Food". Here the cam opens and you can use the AR feature. On the Top is a Information for the user to scan any Product. On the Pictures on the right side is a Potato and a Eis scanned which you can see from the central Headers. On the Main Position is an UI overlay which gives the user some Information such as if its healthy or not as well as some cooking Ideas for this Product.
<br> <br>
   <img src="../../assets/img/_/food4me/pp1/left_tab_cam.jpg" style="width: 90%;">

<br><br>
          On the following you see the middle tab which is about the use case "Cooking". The Grid hase some Plans of different Dishes the user can cook to give some inspiration. After clicking for example on "Wrap" it opens the view on the right. There is a detailed plan of what ingredient categorys it is built. below the Header is even a tipp of how to make it even more healthy.
<br><br>
      <img src="../../assets/img/_/food4me/pp1/blaupause.jpg" style="width: 80%;"> 
<br><br>

          The right tab is to inspire with healthy food. A Grid has the main Food Categorys such as vegetables, fruit and more. Afte4r tapping on one it opens the List on the right picture. 
<br>
   <br>   <img src="../../assets/img/_/food4me/pp1/green_tab.jpg" style="width: 80%;">
<br><br>

          With the hamburger menu on the top right corner the user gets to a main menu, the use case "inform", which incluces informations, settings and hints.
  <br><br>
   <img src="../../assets/img/_/food4me/pp1/menu_tipps_etc.jpg" style="width: 80%;">
   <br> <br>
                          
                              <i style="font-weight: bolder; color: orange;">Paperprototyp 2</i> <br> 
                              <br>

                              The second Prototyp is same in his information architektur and only gives the navigation via menu. It covers the same use cases But The main difference is that at every step via input it tracks the behaviour of the user. This variable i have found in my secondary research of the pain points of user input and behaviour tracking.  
                              <br><br> 
     <img src="../../assets/img/_/food4me/pp2/menuu.jpg" style="width: 20%;">
<br>
   <br>Below you see the use case "Buy food".

   <br><br>
     <img src="../../assets/img/_/food4me/pp2/ar_cam.png" style="width: 80%;">
     <br> <br>

     Following the use case "cooking".

      <br><br>
     <img src="../../assets/img/_/food4me/pp2/cooking.png" style="width: 60%;">
     <br> <br>

     and last use case of "informing". The overviews shows in this case with colors how every day was. if it was a healthy good nutrition day or the person has ate fish etc or red for a unhealthy nutrution day.
   <br><br>
       <img src="../../assets/img/_/food4me/pp2/inform.png" style="width: 80%;">
       <br> <br>
                          
                            
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                            <h6>
                             AB Testing
                            </h6><br>
                            <p>
                              Conducting AB testing of paper prototypes helped to identify usability issues and refine the design of the app. This methodology allowed me to quickly test and iterate on different design concepts, ensuring that the final product is easy to use and visually appealing. The test persons where 6 persons which have been anticipated in the focus group.
                            </p>
                            
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                               Nasa-TLX
                              </h6><br>
                              <p>
                                Using the NASA-TLX method helped to evaluate the overall cognitive load and mental effort required to use the app, also called work load. Results of that quantitative analysis and my qualittative analysis you can see in my <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bachelorthesis</a>.
                              </p>
                              
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                             Interaction Prototype
                              </h6><br>
                              <p>
                                After analysing all Results i used the paperprototyp 1 and did some improvements based on my results. 
                                <br> through some confusions the tabs are changed to the three use cases which where bewertet good about the three buttons in the menu of paperprototyp 2. 
                              </p>
                               Next i programmed an interactive prototype via Unity3D. See <a href="https://gitlab.com/Michelle-P95/food4me" style="color:green">Sourcecode on Gitlab</a><br>
                              <br>
         
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                               Usability Testing
                              </h6><br>
                              <p>
                                Conducting usability testing in a real-world setting, such as a supermarket, helped to identify how users interact with the app in a natural environment. This information was used to refine the design of the app, ensuring that it meets the needs of users in real-life scenarios. 
                              </p>
                              <br>
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                            Attrakdiff
                              </h6><br>
                              <p>
                                Using the Attrakdiff method helped to evaluate the overall user experience of the app, including its usability, aesthetics, and emotional appeal. This methodology allowed me to identify areas where the app excels and areas for improvement, ensuring that the final product is both visually appealing and effective in encouraging long-term healthy eating habits. 
                                See the results in my <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bachelorthesis</a>
                              </p>
                              <br>
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                            Conclusion
                              </h6><br>
                              <p>
                                To see the final developed App click on the Tab "AR/XR".
                              </p>
                              All togehter i got an app which had a high positive evaluation. A lot of technices which i have found while secondary research has been done and via the following diagramm you can see that 100% of all high priority features, 83% of all middle priority and at least 33% of low priority where done.
<br><br>
                                     <img src="../../assets/img/_/food4me/pp2/diagramm_erfuellungsgrad.png" style="width: 80%;">
                              <br>
                                    <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                        <p>
                          Have a Look at <br>
                          ---> <a href="https://miro.com/app/board/uXjVO84jJ7A=/" style="color:green">Miro Board</a><br>
                          ---> <a href="https://gitlab.com/Michelle-P95/food4me" style="color:green">Sourcecode on Gitlab</a><br>
                          ---> <a href="https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing" style="color:green">Bacheloarbeit</a><br>
                          ---> <a href="https://docs.google.com/presentation/d/100CiNBLkK_UFS6s3l89MmtkIJ7EQUjNRSk3DlOmZoJg/edit?usp=sharing" style="color:green">Presentation</a><br>
                        </p>
                       
                     
                    
                    </div>
                    <!-- End description -->
      
                    <!-- <div class="news_share">
                      <Social />
                    </div> -->
                    <!-- End news share -->
                  </div>
                  <!-- End .box_inner -->

                <!-- shane_tm_modalbox_news -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End Modalbox -->
      </li>
<!------------------------------------------------------------------------------------------- AR garten -->
      <li>
  
  <transition name="fade">
    <!-- Modal -->
    <div :class="{ 'modal-mask': isActive2 }" id="modal" @click="closeModal" v-if="isVisible2">
      <div class="modal-dialog modal-dialog-centered " @click.stop>
        <div class="modal-content">
          <div class="close" @click="closeModal">
            <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
          </div>
          <!-- End .close -->
          <div class="shane_tm_modalbox_news">
            <div class="box_inner">
              <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
              <!-- End image -->
              <div class="details">
                <h3 class="title" style="display: block; margin: 0 auto;">
                  Virtual Garden<img src="../../assets/img/_/icons/plant.png" style="height:30px; margin-left: 1em;">
                </h3> 
                
                <p class="date">
                  <a href="#"> </a>
                  <!-- Photoshop, Illustrator, InDesign <span>March 2022</span> -->
                </p>
              </div>
              <!-- End details -->

              <div class="description" style="color: black; font-size: 1rem; ">
               
                <p>This Project is about an Augmented Reality App that aims to address the issue of climate change. The primary objective is to create awareness among people about how their actions impact the environment and encourage them to adopt eco-friendly practices.
                  To reach a wider audience, i decided to develop a smartphone app. Nowadays, almost everyone has a smartphone, starting from teenagers, so it's an accessible medium to connect with people of all ages. 
                </p>

                <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
    
                       
                        <img src="../../assets/img/_/text-info/virtualGarden_info.png" style="display: block; margin: 0 auto; width: 90%;">
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
  <div class="description" style="color: black; font-size: 1.4em; text-decoration: underline; font-weight: bold;">Process</div>
  <br> 
                        <img src="../../assets/img/_/text-overview/overview_argarden.png" style="width: 50%">
                      <br>
                    
                    
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                
                 

               
                              <br>
                              <h6>
                                Focusgroup 
                              </h6><br>
                              <p>
                                Conducting a focus group allowed me to gather insights on the target audience's behavior and attitudes towards environmental impact. I was able to identify pain points and opportunities to motivate individuals to change their behavior using the augmented reality app. See all the data in my <a href="">Excel Sheet</a>. 
                              </p>
                              <br>                
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 

  <br>
                                <h6>
                                  Empathy Map
                                </h6><br>
                                <p>
                                  By creating an empathy map, I was able to understand the emotions, thoughts, and behaviors of the target audience. This helped me to design an app that resonates with the user's values and motivates them to take positive actions towards the environment.
                                </p>
                                <br>  

                
              
                <img src="../../assets/img/_/ux/virtual Garden - Empathy Map.png" style="display: block; margin: 0 auto; width: 90%;">
                
              <br>

               <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                
        

               
                              <br>
                              <h6>
                                Problem Statement 
                              </h6><br>
                              <p>
                               People require a user-friendly solution that allows them to easily understand their behaviours climate change impact as well as inspiration how to easy change to similar changes. This is crucial in order to avoid making decisions which are bad for the enviroment and not having the conscious decision to choose a better choice for the climate.
                              </p>
                              <br>                

                               <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                
                 

               
                                <br>
                                <h6>
                                  Goal Statement 
                                </h6><br>
                                <p>
                                  The App will let users show them visualy how their behaviour change the climate to the bad which will help to understand their impact and get Ideas how to change easy to better decisions for the climate.
                                </p>
                                <br>                

               <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
              <br>
                <h6>
                Storyboard
                </h6><br>
              <p>
            Storyboarding allowed me to visualize the user's journey with the app, identifying potential issues and opportunities to improve the user experience. This helped me to create a seamless and engaging experience for the user.
              </p>
              <br> 

                <br>
                  <img src="../../assets/img/_/ux/virtual Garden - Storyboard.png" style="display: block; margin: 0 auto; width: 80%;">
                <br>
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                <br>
                  <h6>
                  User Flow
                  </h6><br>
                <p>
                 Creating a user flow helped me to understand the steps that the user needs to take to achieve their goals using the app. By mapping out the user flow, I was able to identify potential roadblocks and design solutions that simplify the user journey. This increases the likelihood that users will take the desired actions and reduce their environmental impact. 
                </p>
                <br> 
 
                <br>
                <img src="../../assets/img/_/ux/virtual Garden - User Flow.png" style="display: block; margin: 0 auto; width: 100%;">
                <br>
    <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                <br>
                    <h6>
                    Paperprototyp
                    </h6><br>
                  <p>
                    With my analysed insights i designed a paperprototype. See below for some impressions.<br>
                       First you see a Garden which will be placed via Augmented Reality in your Roome. It has some elements such as Trees and a Sea. There is also a little House which is markes as Home.
                  </p>
                  <br> 

                <img src="../../assets/img/_/paperprototype/garden.png" width="100%"> <br><br>

                 <br>
                      <p>
                      if there is a change to the clima of your Inputs of your behaviour it will be displayed with a red Icon and a speach bubble when you click on it so you see what happened and why.
                      </p>
                  <br>

                <img src="../../assets/img/_/paperprototype/negative_change.png" width="40%" style="margin-right: 50px;">
                <img src="../../assets/img/_/paperprototype/negative_change_info.png" height="300 vh"> <br><br>

                <br>
                        <p>
                        The same is with a positive Outcome but with a green Tic.
                        </p>
                    <br>

                 <img src="../../assets/img/_/paperprototype/postive_change.png" width="40%" style="margin-right: 50px;">
                <img src="../../assets/img/_/paperprototype/positive_change_info.png" height="300 vh"> <br><br>

                <br>
                        <p>
                        When clicking on the Home-House you come to the Main-Menu which can lead you to the AR-Garden or the Logbook of all your Past Inputs. 
                        The "+" button gets you the right Menu where you can make new Inputs.
                        </p>
                    <br>
                 <img src="../../assets/img/_/paperprototype/menu.png" height="300 vh" style="margin-right: 30px;">  
                <img src="../../assets/img/_/paperprototype/logbook.png" height="300 vh" style="margin-right: 30px;">  
                <img src="../../assets/img/_/paperprototype/add_item.png" height="300 vh">
<br><br>
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 

   
                     <br>
                      <h6>
                      Evaluation 
                      </h6><br>
                    <p>
                      Through testing a paper prototype with 5 individuals, I was able to identify usability issues and make improvements to the design. Feedback was used to refine the design, ensuring that the augmented reality app is easy to use and visually appealing.
                    The traffic light colors were quite positive, so the color yellow, which signifies "attention," was added to highlight important information, such as tips for capturing action shots for the user.
                    </p>
                    <br>                    
<br>
                          <img src="../../assets/img/_/paperprototype/new_changes.png" height="300 vh">

                        <br><br>
                            <p>
                            Due to a misunderstanding, the term 'Logbook' was changed to 'Tagebuch,' which means 'Diary' in German. Additionally, during testing, some users asked 'Which garden?' in response to certain questions. To address this, we added the possessive adjective 'My' to create 'My Garden,' emphasizing that the environmental impact is the result of the user's behavior.
                            </p>
                        <br>
                          <img src="../../assets/img/_/paperprototype/new_menu.png" height="300 vh">
                          <br>
                           <br> 
      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>  <br>
                        <h6>
                        Interaction Prototype
                        </h6><br>
                      <p>
                         Based on the feedback from the paper prototype testing, an interactive prototype was developed using Unity. With the vuforia sdk the AR features were implemented. This prototype allowed users to experience the augmented reality app in a more realistic and immersive way, and provided valuable insights into how users interact with the app.
          
                      </p>

                      <p>Following you can see the UI Menus. Left the Startmenu, second the Logbook and right two Screens when the user makes an Input with a Dropdown Menu and gets a user Feedback when it was added successful.  </p>
                      <br> 

                      <img src="../../assets/img/_/paperprototype/final/startmenu.png" height="300 vh" style="margin-right: 30px;">
                      <img src="../../assets/img/_/paperprototype/final/logbuch.png" height="300 vh" style="margin-right: 30px;">    
                      <img src="../../assets/img/_/paperprototype/final/dropdown.png" height="300 vh" style="margin-right: 30px;">  
                      <img src="../../assets/img/_/paperprototype/final/added.png" height="300 vh" style="margin-right: 30px;">  
                      

                      <br><br>
                      
                      <p>
                        The Button on the Top brings to the 3D virtual Garden which will be placed via AR in the real physics World of the User via Camera. You can see the Garden below.
                      </p>

                      <br>
                      <img src="../../assets/img/_/paperprototype/final/Garden - good condition.png" height="300 vh" style="margin-right: 30px;">  

                      <br><br>
                      
                        <p>
                         Positive and Negative Changes are implemented like the design of the paperprototype. 
                        </p>


                      <img src="../../assets/img/_/paperprototype/final/Best condition Tree.png" height="300 vh" style="margin-right: 30px;">  
                      <img src="../../assets/img/_/paperprototype/final/changed negativ.png" height="300 vh" style="margin-right: 30px;">  

                      <br><br>
                      
                          <p>
                          Clicking on the Yellow Sign brings the User to the UI below. Here are with green Speachbubbles are notet down which behaviour made what positive outcome. The red Speachbubble says which behaviour made a negative impact on the Enviroemnt and a Tipp how to change this behaviour. On the Right you can see the Garden in his worst Condition.
                          </p>
              
                      <img src="../../assets/img/_/paperprototype/final/UI - Info.png" height="300 vh" style="margin-right: 30px;"> 
                       <img src="../../assets/img/_/paperprototype/final/Garden - bad condition.png" height="300 vh" style="margin-right: 30px;">   

                      
                      <br>

     <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>                       

                      <br>  
                          <h6>
                          Heuristic Evaluation
                          </h6><br>
                        <p>
                           A heuristic evaluation was conducted with 5 different individuals to identify usability issues and areas for improvement in the app. This evaluation helped to ensure that the app meets industry standards for usability and provided valuable insights into how to optimize the user experience. The Changes where mainly about the placing via AR in the World for a better imersive Experience.
                           <br>
                           <br>
                           
  Since testing the usability of Augmented Reality features with paper prototypes is not feasible, feedback for the Garden AR feature could only be collected during the evaluation of the digital prototype. Based on the testers' inquiries about using this feature, the UI was expanded to include a prompt to click on a surface to place the garden. (See image below) This helps provide clear and simple instructions to the user, alleviating any uncertainty. This is especially important as the use of Augmented Reality is still relatively new and not widely familiarized.
                        </p>
                        <br> 
                        <img src="../../assets/img/_/paperprototype/evaluation_ar.png" height="300 vh" style="margin-right: 30px;"> <br>

<br>
                        <b>See the final App in the "AR/XR" Tab.</b> <br>

    <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 

     <br>  
                            <h6>
                            Conclusion
                            </h6><br>
                          <p>
                             The development of this augmented reality app aimed at promoting positive environmental behavior has been a great success. Through the use of various UX design methods, it was able to create an app that is intuitive, engaging, and effective at motivating behavior change. The addition of features such as "My Garden" and the use of clear and concise language in the user interface has further enhanced the user experience.
                          </p>
                          <br> 


      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 




    <br>  
                            <h6>
                            Final Sources
                            </h6><br>
                          <p>
                             
                          </p>
                     
                           ----> See here the <a href="https://github.com/Michelle-P95/AR-virtual-Garden">Project on Github</a> to see scripts, presentation, documentation and some design/development Impressions.<br> 
                      
                  


              </div>
              <!-- End description -->

              <!-- <div class="news_share">
                      <Social />
                    </div> -->
              <!-- End news share -->
            </div>
            <!-- End .box_inner -->
          </div>
          <!-- shane_tm_modalbox_news -->
        </div>
      </div>
    </div>
  </transition>
  <!-- End Modalbox -->
      </li>
<!------------------------------------------------------------------------------------------ Tattoo app -->
<li>
  <transition name="fade">
    <!-- Modal -->
    <div :class="{ 'modal-mask': isActive3 }" id="modal" @click="closeModal" v-if="isVisible3">
      <div class="modal-dialog modal-dialog-centered " @click.stop>
        <div class="modal-content">
          <div class="close" @click="closeModal">
            <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
          </div>
          <!-- End .close -->
          <div class="shane_tm_modalbox_news">
            <div class="box_inner">
              <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
              <!-- End image -->
              <div class="details">
                <h3 class="title">
                  Tattoo App<img src="../../assets/img/_/icons/blackHeart.png" style="height:30px; margin-left: 1em;">
                </h3>
                <p class="date">
                  <a href="#"> </a>
                 <!--  Photoshop, Illustrator, InDesign <span>March 2022</span> -->
                </p>
              </div>
              <!-- End details -->

              <div class="description" style="color: black; font-size: 1rem; ">
                 
                  <p>This Project is about a App with the aim to help people who are either planning to get a tattoo or are already thinking about it.
  The main goal is to provide a platform where users can easily find the right tattoo artist and book appointments without any hassle. 
                  </p>
  
                  <img src="../../assets/img/_/text-info/stillInProgress.png" style="height: 5em;">
                  <br>
                  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
      
                         
                          <img src="../../assets/img/_/text-info/tattooapp_info.png" style="display: block; margin: 0 auto; width: 90%;">
    <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
    <div class="description" style="color: black; font-size: 1.4em; text-decoration: underline; font-weight: bold;">Process</div>
    <br> 
                          <img src="../../assets/img/_/text-overview/overview_tattooapp.png" style="width: 30%">
                        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                    <br>
                        <h6>
                        User Interviews
                        </h6><br>
                      <p>
  To start my project which getting data and understanding the needs of potential users, i conducted user interviews with 7 individuals who expressed interest in getting a tattoo. These interviews provided valuable insights into their needs, preferences, and expectations regarding tattoo services. The feedback gathered from these interviews has been pivotal in shaping the design and features of the app to cater to the unique requirements of the personas I have developed.</p>
                      <br> 
                      
      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                  <br>
                      <h6>
                      Personas
                      </h6><br>
                    <p>Through my collected insight i have identified three primary user groups. These personas served as a foundation for developing user-centered design solutions that meet the needs of all groups.</p>
                    <br> 
                

                    
                <img src="../../assets/img/_/ux/Tattoo App - Persona 1.png" width="90%" style="display: block; margin: auto">
                <img src="../../assets/img/_/ux/Tattoo App - Persona 2.png" width="90%" style="display: block; margin: auto">
                <img src="../../assets/img/_/ux/Tattoo App - Persona 3.png" width="90%" style="display: block; margin: auto">
                <br>

                 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                    <br>
                        <h6>
                        Empathy Map
                        </h6><br>
                      <p>To better understand the emotions, thoughts, and behaviors of all different types of users, I created an empathy map. This helped me understand the users' needs and the barriers they face when seeking a tattoo artist. By using the empathy map, I was able to identify the users' pain points and develop solutions to overcome them.</p>
                      <br> 
              

               
                
                <br>
                <img src="../../assets/img/_/ux/Tattoo App - Empathy Map.png" width="95%" style="display: block; margin: auto">
                <br>

                 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                      <br><h6>
                            User Stories
                            </h6><br>
                      
                
        
               


<ul  style="list-style-type:disc;">
  <li>As a user looking for a tattoo, I want to be able to search for tattoo artists based on their specific tattoo style, so I can find an artist whose work aligns with my desired aesthetic.</li>

  <li>As a user wanting a tattoo, I want to be able to locate tattoo artists near my current location, allowing me to find artists conveniently and reduce travel time.</li>

  <li>As a user seeking a tattoo, I want to be able to view the availability of tattoo artists and book appointments directly through the app, making it easier to secure a time slot that works for both me and the artist.</li>

  <li>As a user exploring tattoo options, I want to be able to browse through a tattoo artist's portfolio, viewing their previous work and gaining confidence in their artistic abilities.</li>

 <li> As a user interested in getting a tattoo, I want to be able to read and leave reviews for tattoo artists, enabling me to make informed decisions and choose the right artist for my needs.</li>

  <li>As a user scheduling a tattoo, I want to be able to communicate with the chosen tattoo artist through the app, exchanging drawings, discussing details, and organizing all necessary information in one central place.</li>
  </ul>
  <br>
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 

                          <h6>
                          Storyboard
                          </h6><br>
                      <p>To create a visual representation of the user's journey, I developed a storyboard. This helped me visualize the user's experience with the app from start to finish. By creating a storyboard, I was able to identify potential usability issues and design solutions to improve the user experience</p>

                        
               
                <br>
                <img src="../../assets/img/_/ux/Tattoo App - Storyboard.png" width="90%" style="display: block; margin: auto">
                <br>

                 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                      <br>
                          <h6>
                          User Flow
                          </h6><br>
                      <p>To create a seamless user experience, I developed a user flow that shows the user's path through the app. This user flow helped me identify areas of the app where the user may get lost or confused. By analyzing the user flow, I was able to make design decisions that guide the user and improve the overall experience.</p>
                        <br>     
                
                <br>
                <img src="../../assets/img/_/ux/Tattoo App - User Flow.png" width="100%" style="display: block; margin: auto">
                <br>
   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                      <br>
                          <h6>
                          Wireframes
                          </h6><br>
                     
                        <p>Following some Wireframes. But here a just some impressions. As the Project is still in progress...</p>
                        <br>

  <img src="../../assets/img/_/ux/Tattoo App - Wireframes.png" width="100%" style="display: block; margin: auto">
               <!--      <p>In conclusion, the app design project involved employing several UX design methods, including personas, empathy maps, storyboards, and user flows. By using these methods, I was able to create a user-centered design that meets the needs of both first-time tattoo seekers and experienced tattoo enthusiasts. I believe that the app will provide a convenient and enjoyable experience for users seeking to find a suitable tattoo artist.</p>    -->
    
                <br>
              
              </div>
              <!-- End description -->

              <!-- <div class="news_share">
                      <Social />
                    </div> -->
              <!-- End news share -->
            </div>
            <!-- End .box_inner -->
          </div>
          <!-- shane_tm_modalbox_news -->
        </div>
      </div>
    </div>
  </transition>
  <!-- End Modalbox -->
</li>

<!------------------------------------------------------------------------------------------ AR restaurant -->
<li>
  <transition name="fade">
    <!-- Modal -->
    <div :class="{ 'modal-mask': isActive4 }" id="modal" @click="closeModal" v-if="isVisible4">
      <div class="modal-dialog modal-dialog-centered " @click.stop>
        <div class="modal-content">
          <div class="close" @click="closeModal">
            <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
          </div>
          <!-- End .close -->
          <div class="shane_tm_modalbox_news">
            <div class="box_inner">
              <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
              <!-- End image -->
              <div class="details">
                <h3 class="title">
                          ARestaurant<img src="../../assets/img/_/icons/koch.png" style="height:30px; margin-left: 1em;">
                        </h3>
                        <p class="date">
                          <a href="#"> </a>
                     
                        </p>
                     
  
                      
  </div>
                      <div class="description" style="color: black; font-size: 1em;">
  
                         <p>This is a Project about an App designed to revolutionize the dining experience in restaurants. By harnessing the power of augmented reality, this app aims to assist customers in making informed choices by visually presenting virtual dishes on their tables. With the ubiquity of smartphones, users can conveniently access this app to ensure they make the right choice and have their expectations fulfilled while dining out.
                          
                         

              
                            </p>
  
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>

                        
    
                       
                        <img src="../../assets/img/_/text-info/arestaurant_info.png" style="display: block; margin: 0 auto; width: 85%;">
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
    <div class="description" style="color: black; font-size: 1.4em; text-decoration: underline; font-weight: bold;">Process</div>
                        <img src="../../assets/img/_/text-overview/overview_arestaurant.png" style="width: 50%">
                      <br>
                    
                <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
                   <br>  
                                <h6>
                                Survey
                                </h6>

                  <br>
                    <p>
                      Through the main purpose of this project which is about ordering food in a restaurant almost any person is a potential user. So i decided to do a survey via google forms to get as much participants as possible. I shared my survey via social Media and had at the end a summary of 86 participants.
                    </p>
                  <br>
                
                
              <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
                 <br>  
                              <h6>
                              Personas
                              </h6>

                <br>
                  <p>
                    As next step to empatize and get in the shoes of the people, i evaluated my collected data and identified two primary user groups for the app. Following you see my created Personas.
                  </p>
                <br>

                <img src="../../assets/img/_/ux/ARestaurant - Persona 1.png" width="80%" style="display: block; margin: auto">
                  <img src="../../assets/img/_/ux/ARestaurant - Persona 2.png" width="80%" style="display: block; margin: auto">
              
                <br>

                <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
                     <br>  
                                  <h6>
                                  Problem Statement
                                  </h6>

                    <br>
                      <p>
                       One common challenge faced by diners in restaurants is the difficulty in making informed choices from an extensive menu. Traditional menus often provide limited information and rely heavily on textual descriptions, leaving customers uncertain about the appearance and presentation of the dishes they are considering. This lack of visual context can lead to disappointment and unsatisfactory dining experiences. Summarized i got the following Problem Statement: <br>
                     <i style="color:darkorange">Restaurant customers require a user-friendly solution that allows them to easily visualize virtual dishes, understand portion sizes, identify specific ingredients, and gain a comprehensive understanding of the potential meal they are about to order. This is crucial in order to avoid making incorrect choices and ensure that their expectations are met, leading to a satisfying dining experience.
                     </i> </p>
                    <br>

                      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>

               
                       <br>  
                                    <h6>
                                    Goal Statement
                                    </h6>

                      <br>
                        <p>
                            this brings us to following goal statement: 
                       <i style="color:darkorange">The App will let users visualise dishes of a menu which will help restaurant customers by understanding meals and their sizes, portions of ingredients and help to make their right choice as well as editing their meal to their personal preferences.
                       </i> </p>
                      <br>

                      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>

                    <br>  
                      <h6>
                        User Stories
                      </h6> <br>

                      <p> 
                        <ul style="  list-style-type: disc;">
                        <li>As a restaurant guest, I want to be able to see a 3D model of each dish on the menu card using augmented reality (AR), in order to have a better idea of the presentation and appearance of the dish.</li>
 
                            <li> As a restaurant guest, I want the option to directly order the selected dish from the AR view through the app, to make the ordering process convenient and seamless.</li>
                               
                            <li> As a restaurant guest, I want to be able to make specific modifications to a dish by adding or removing ingredients or providing special preparation instructions while viewing the 3D model in the AR view, in order to customize my dish according to my specific preferences.</li>
                                </ul>
                        

                        </p>
                  <br>
                

          
                        <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>

                  <br>  
                    <h6>
                      Storyboard
                    </h6> <br>

                    <p>
                      To create a visual representation of the user's journey, I developed a storyboard. This helped me visualize the user's experience with the app from start to finish. By creating a storyboard, I was able to identify potential usability issues and design solutions to improve the user experience.
                    </p>
                <br>
                
              
                <img src="../../assets/img/_/ux/ARestaurant - Storyboard.png" width="80%" style="display: block; margin: auto">
          
                 <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>

                  <br>  
                      <h6>
                        Brainstorming
                      </h6> <br>

                      <p>
                        To get some Ideas of how to design the interaction of the menu card of the restaurant i did some brainstorming and finally decided to make the tracking via image tracking and designed the following Menu cards. 
                      </p>

                         <img src="../../assets/img/_/ux/arestaurant_menucards.png" width="100%" style="display: block; margin: auto">
                  <br>
                 

                   <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
                   <br>  
                        <h6>
                          Prototyp
                        </h6> <br>

                        <p>
                          Through the focus of developing/coding the app there was after creating the app no testing afterwards. 
                        </p>

                         <p>
                               <b>See the final App in the "AR/XR" Tab.</b> 
                          </p>
                           <p>
                  ----> click here to see the <a href="https://github.com/Michelle-P95/AR-Restaurant-Menu">Sourcecode on Github</a><br>
                  </p>
                    
 
           
               
              
              </div>

              
              <!-- End description -->

              <!-- <div class="news_share">
                      <Social />
                    </div> -->
              <!-- End news share -->
            </div>
            <!-- End .box_inner -->
          </div>
          <!-- shane_tm_modalbox_news -->
        </div>
      </div>
    </div>
  </transition>
  <!-- End Modalbox -->
</li>

<!------------------------------------------------------------------------------------------ Design magazin -->
<li>
  <transition name="fade">
    <!-- Modal -->
    <div :class="{ 'modal-mask': isActive5 }" id="modal" @click="closeModal" v-if="isVisible5">
      <div class="modal-dialog modal-dialog-centered " @click.stop>
        <div class="modal-content">
          <div class="close" @click="closeModal">
            <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
          </div>
          <!-- End .close -->
          <div class="shane_tm_modalbox_news">
            <div class="box_inner">
              <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
              <!-- End image -->
              <div class="details">
                <h3 class="title">
                  Design - Magazin Article

                </h3>
                <p class="date">
                  <a href="#"> </a>
                  Photoshop, Illustrator, InDesign <span>March 2022</span>
                </p>
              </div>
              <!-- End details -->

              <div class="description" style="color: black; font-size: 17px;">
                <ul style="list-style-type:disc; list-style-color: black; ">
               
              
                </ul>
             
                
              
              
                <p>
                  I have designed a Cover and an Article over 3 Pages. The Topic was Mindset. <br>
                  First i have made some sketches of Layout i like, Color Palettes and collected some free license Pictures i may use later. <br>
                  After having some Ideas of Concepts, i made with Photoshop of five stock Images (which are seen on the right side) one composition which i wanted to use in my Magazin Design later.
                </p>
                <br>

              <img src="../../assets/img/_/Design/PS.jpg" width="80%">
               <br>   <br>
                  <p>
                    Next step i created an vector Graphic in Illustrator also for using that later too. <br>
                    I brainstormed about the Idea and used similar Colores to my Photoshop composition.
                  </p>
                  <br>
                <img src="../../assets/img/_/Design/Illustrator_Sign.png" width="80%"> <br><br>

               
                <p>
                  Finaly i created my InDesign File. I wrote some paragraphs down of my favourite Book (How to not give a F*ck - Mark Manson) and placed the whole Text as one on the Pages first. In various Interations i played with different Ideas though i came the my final Design. <br>
                  
                </p>
                <br>

                <img src="../../assets/img/_/Design/Mockup-Magazin.jpg">

                <br>     <br>
                <p>
                 Cause i am a very music loving person i created a Spotify Playlist which communicates the Vibe i wanted to create with this Magazin Design and placed it on one Page. <br>
                 Listen to it and i am happy to hear your Feedback about matching the Music with my Magazin Article Design ! :)
                </p>

              

                
              
              </div>

                
             
              <!-- End description -->

              <!-- <div class="news_share">
                      <Social />
                    </div> -->
              <!-- End news share -->
            </div>
            <!-- End .box_inner -->
          </div>
          <!-- shane_tm_modalbox_news -->
        </div>
      </div>
    </div>
  </transition>
  <!-- End Modalbox -->
</li>

<!------------------------------------------------------------------------------------------ CAD -->
<li>
  
  <transition name="fade">
    <!-- Modal -->
    <div :class="{ 'modal-mask': isActive6 }" id="modal" @click="closeModal" v-if="isVisible6">
      <div class="modal-dialog modal-dialog-centered " @click.stop>
        <div class="modal-content">
          <div class="close" @click="closeModal">
            <img class="svg" src="../../assets/img/svg/cancel.svg" alt="cancel-img" />
          </div>
          <!-- End .close -->
          <div class="shane_tm_modalbox_news">
            <div class="box_inner">
              <!-- <div class="image">
                      <img src="" alt="thumb" />
                      <div class="main" :style="{ backgroundImage: 'url(' + imgMagazin + ')' }"></div>
                    </div> -->
              <!-- End image -->
              <div class="details">
                <h3 class="title">
                  CAD
                </h3>
                <p class="date">
                  <a href="#"> </a>
                  <!-- Photoshop, Illustrator, InDesign <span>March 2022</span> -->
                </p>
              </div>
              <!-- End details -->

              <div class="description" style="color: black; font-size: 17px;">
                <ul style="list-style-type:disc; list-style-color: black; ">
                  <li>Fokusgruppe</li>
                  <li>Low-Fidelity (Paperprototyp)</li>
                  <li>A/B Testing</li>
                  <li>Nasa TLX</li>
                  <li>High-Fidelity (Unity)</li>
                  <li>Usability Test</li>
                  <li>Attrakdiff</li>
              
                </ul>
                <br>
                <ul style="list-style-type:disc; list-style-color: black; ">
                  <li>Understand == Researche (Empathise & Define)</li>
                  <li>Ideate / Design</li>
                  <li>Develop == Protoyp</li>
                  <li>Test</li>
                </ul>
                <br>
              
                <p>
                  <a href="">Presentation</a><br>
                  <a href="">Documentation</a><br>
                  <a href="">Miro Board</a><br>
                  <a href="">Sourcecode on Github</a><br>
                </p>
              
                <br>
                <p>
                  Paragraph 1
                </p>
              
                <br>
                <video id="videoFaster" width="20%" muted controls>
                  <source src="../../assets/img/_/AR/bubble_hat.mp4" type="video/mp4">
                  Your browser does not support the video tag.
                </video>
                <br>
              
                <p>
                  Paragraph 2
                </p>
              
                <br>
                <img src="../../assets/img/_/ux/virtual Garden - User Flow.png" style="display: block; margin: 0 auto; width: 100%;">
                <br>
              
                <p>
                  Paragraph 3
                </p>
              
                <br>
                <img src="../../assets/img/_/ux/virtual Garden - Storyboard.png" style="display: block; margin: 0 auto; width: 80%;">
                <br>
              
                <p>
                  Paragraph 4
                </p>
              
              </div>
              <!-- End description -->

              <!-- <div class="news_share">
                      <Social />
                    </div> -->
              <!-- End news share -->
            </div>
            <!-- End .box_inner -->
          </div>
          <!-- shane_tm_modalbox_news -->
        </div>
      </div>
    </div>
  </transition>
  <!-- End Modalbox -->
</li>

    </ul>
    </div>
  
</div>
</template>

<script>
export default {
  data() {
    return {
      activetab: 2,
// ----------------------------------------------------------------------------- AR      
      arVrItems: [
        {
          src: require("../../assets/img/_/AR/food4me_clideo.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/Food4Me.png"),
          portfolioName: "AR App - Food4Me",
          //portfolioType: "AR",
          play: require("../../assets/img/_/play.png"),
          details: "made with User-Centered-Design in Unity3D. AR at 1:12min in video.",
          buttn1: "",
          buttn1url: "https://gitlab.com/Michelle-P95/food4me/-/tree/master/Assets/Scripts",
          buttn2: "",
          buttn2url: "https://miro.com/app/board/uXjVO84jJ7A=/?share_link_id=711999834215",
          buttn3: "",
          buttn3url: "https://docs.google.com/document/d/1mUVoPpCGsO9plmABnNau5JqEvXcva0iUBgEd1U8KJqI/edit?usp=sharing",
        },
        {
          src: require("../../assets/img/_/AR/video_virtualGarden_480p.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/virtualGarden.png"),
          portfolioName: "AR App - virtual Garden",
          details: "made with User-Centered-Design in Unity3D with Houdini.",
          buttn1: "",
          buttn1url: "https://github.com/Michelle-P95/AR-virtual-Garden",
          buttn2: "",
          buttn2url: "https://docs.google.com/presentation/d/1SL2Gy09P8xkqmmcojsxeu_8KxlBxlH3Fz21RGC8swIY/edit?usp=sharing",
          buttn3: "",
          buttn3url: "",
        },
        {
          src: require("../../assets/img/_/AR/Handtracking.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/HandtrackingXR.png"),
          portfolioName: "XR / VR - Handtracking",
          //portfolioType: "XR",
           details: "made in Unity3D with Leapmotion, SteamVR.",
          buttn1: "",
          buttn1url: "",
          buttn2: "",
          buttn2url: "",
          buttn3: "",
          buttn3url: "",
        },
          {
          src: require("../../assets/img/_/AR/ARestaurant_x1.8.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/ARestaurant.png"),
          portfolioName: "AR App - ARestaurant",
          //portfolioType: "AR",
          details: "made in Unity3D with Vuforia SDK.",
          buttn1: "",
          buttn1url: "",
          buttn2: "",
          buttn2url: "",
          buttn3: "",
          buttn3url: "",
        },
        {
          src: require("../../assets/img/_/AR/milka_video2.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/milka3.png"),
          portfolioName: "AR - Object Tracking",
           details: "made in Meta Spark Studio. The chocolate models and their animations i have made in Blender.",
        },
          {
          src: require("../../assets/img/_/AR/video_conch.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/magic_conch.png"),
          portfolioName: "AR - Face Tracking",
          details: "made in Lens Studio. Randomizer and triggers with Touch.",
          additional: "used over 700k times in Snapchat.",
        },
        {
          src: require("../../assets/img/_/AR/video_final_burger.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/burger.png"),
          portfolioName: "AR - Face Tracking",
           details: "made in Lens Studio. triggers with a kiss mouth.",
               additional: "used over 400k times in Snapchat.",
        },
        {
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/bubble_hat.png"),
              portfolioName: "AR - Face Tracking",
                 details: "made in Lens Studio. triggers with open Mouth.",
                 additional: "used over 200k times in Snapchat.",
        },
         
        {
          src: require("../../assets/img/_/AR/YouVSWild.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/YouvsWild.png"),
              portfolioName: "AR - Face Tracking",
                  details: "made in Lens Studio with visual Scripting. triggers with 'open Mouth' Animations, Sounds and more.",
    
          
        },
      
        
      
      ],
// ----------------------------------------------------------------------------- design      
      designItems: [
        {
          src: require("../../assets/img/_/Design/Illustrator_Sign.png"),
          thumb: require("../../assets/img/_/Design/Illustrator_Sign.png"),
          portfolioName: "Graphic Design",
          //portfolioType: "Design",
          details: "made in Illustrator."
        },
        {
          src: require("../../assets/img/_/Design/UX - Grafik - JobsToBeDone.jpg"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - JobsToBeDone.jpg"),
          portfolioName: "Illustration",
          //portfolioType: "Illustration",
          details: "about the Framwork 'Jobs-to-be-done'.",
        },
        {
          src: require("../../assets/img/_/Design/UX - Grafik - DesignMindset.jpg"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - DesignMindset.jpg"),
          portfolioName: "Illustration",
          //portfolioType: "",
          details: "about the Framwork 'Design Thinking'.",
        },

        {
          src: require("../../assets/img/_/Design/UX Design - My Story.jpg"),
          thumb: require("../../assets/img/_/Design/UX Design - My Story.jpg"),
          portfolioName: "Illustration",
          details: "about my Story about lerning Process of Ux-Desing Theorie. made in Photoshop with Miro.",
        },
        {
          src: require("../../assets/img/_/Design/UX - Grafik - UXProcess.jpg"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - UXProcess.jpg"),
          portfolioName: "Illustration",
          details: "about the UX-Process.",
        },
         {
          src: require("../../assets/img/_/AR/preview.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/neon-pink.png"),
          portfolioName: "Glitch Art Filter",
          details: "made in Lens Studio. can be used in Snapchat.",
        },
        
      ],

// ----------------------------------------------------------------------------- 3D   
      dreiDItems: [
        {
          src: require("../../assets/img/_/3D/video-3d-game.mp4"),
            autoplay: true,
          thumb: require("../../assets/img/_/3D/mockup_3D-Game.png"),
          portfolioName: "3D Game - Überkochen",
          details: "made in Unity3D. up to 4 Players.",
        }, 
        {
          src: require("../../assets/img/_/3D/video-2D-game.mp4"),
            autoplay: true,
          thumb: require("../../assets/img/_/3D/2D-Game.png"),
          portfolioName: "2D Game",
          details: "made in Unity3D. Adventure Game.",
        },
        {
          src: require("../../assets/img/_/3D/recorder.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/3D/taperecorder2.png"),
          portfolioName: "3D Model - Maya",
          details: "made in Maya. I have made various Models. I have worked here with Groups and according given requirements.",
        },
        {
          src: require("../../assets/img/_/3D/Bierkrug.jpg"),
          thumb: require("../../assets/img/_/3D/Bierkrug.jpg"),
          portfolioName: "Rendering - Maya",
          details: "made in Maya. I have made various Models. I have done here modelling, texturing, lightning and rendering.",
        },
        {
          src: require("../../assets/img/_/3D/gameboy.png"),
          thumb: require("../../assets/img/_/3D/gameboy.png"),
          portfolioName: "3D Model - Blender",
          details: "made in Blender. I have done modelling, texturing and animations.",
        },
        {
          src: require("../../assets/img/_/3D/catia_cad.jpg"),
          thumb: require("../../assets/img/_/3D/catia_cad.jpg"),
          portfolioName: "CAD - Catiav5/Autocad",
          details: "experiene 3 years as product designer for Audi. including part design, generative shape design, assembly design, technical drawings.",
        },

      ],
      index: null,
      isActive: false,
      isVisible: false,
      isActive2: false,
      isVisible2: false,
      isActive3: false,
      isVisible3: false,
      isActive4: false,
      isVisible4: false,
      isActive5: false,
      isVisible5: false,
      isActive6: false,
      isVisible6: false,
    };
  },
  methods: {
    showModal1: function () {
      this.isActive = true;
      this.isVisible = true;
    },
    showModal2: function () {
      this.isActive2 = true;
      this.isVisible2 = true;
    },
    showModal3: function () {
      this.isActive3 = true;
      this.isVisible3 = true;
    },
    showModal4: function () {
      this.isActive4 = true;
      this.isVisible4 = true;
    },
    showModal5: function () {
      this.isActive5 = true;
      this.isVisible5 = true;
    },
    showModal6: function () {
      this.isActive6 = true;
      this.isVisible6 = true;
    },
    closeModal: function () {
      this.isActive = false;
      this.isVisible = false;
      this.isActive2 = false;
      this.isVisible2 = false;
      this.isActive3 = false;
      this.isVisible3 = false;
      this.isActive4 = false;
      this.isVisible4 = false;
      this.isActive5 = false;
      this.isVisible5 = false;
      this.isActive6 = false;
      this.isVisible6 = false;
    },
    playVideo(event) {
       event.target.play();
    }
  }
};
</script>

<style lang="scss" scoped></style>

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

      <div style="color: limegreen;"><i>click on any image to see a video presentation</i></div>
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
          <li>
            <div class="inner" @click="showModal1">
              <div class="">
                <img class="image" src="../../assets/img/_/AR/Food4Me.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>Food4me</h3>
                <span>UX</span>
              </div>
            </div>
          </li>

          <li>
            <div class="inner" @click="showModal2">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/AR/virtualGarden.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>Virtual Garden</h3>
                <span>UX</span>
              </div>
            </div>
          </li>

          <li>
            <div class="inner" @click="showModal3">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/ux/Tattoo App - Empathy Map.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>Tattoo App</h3>
                <span>UX</span>
              </div>
            </div>
          </li>

          <li>
            <div class="inner" @click="showModal4">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/AR/ARestaurant.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                         <img src="../../assets/img/_/open.png" alt="Play Icon">
                  </div>
            </div>
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

            <button v-if="image.buttn" class="custom-button-green" href='https://github.com/Michelle-P95/XR-Handtracking'>{{ image.buttn }}</button>
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
                  <img class="image" src="../../assets/img/_/Design/Mockup-Magazin.png" alt="Portfolio" />
                </div>
                <!-- End .entry -->
                <div class="mobile_title">
                  <h3>Magazine Article (Indesign)</h3>
                  <span>Design</span>
                </div>
              </div>
            </li>

          <li v-for="(image, imageIndex) in designItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
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

          <li v-for="(image, imageIndex) in dreiDItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>

          <li>
            <div class="inner" @click="showModal6">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" src="../../assets/img/_/3D/catia_cad.png" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>(CatiaV5)</h3>
                <span>CAD</span>
              </div>
            </div>
          </li>
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
                      <img src="../../assets/img/_/text-overview/overview_food4me.png" style="width: 50%">
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
                          Paper Prototyp
                            </h6><br>
                            <p>
                              Creating two paper prototypes with a variable difference allowed me to compare and evaluate two different design concepts quickly and efficiently. _____________________________________________
                            
                            </p>
                            <br>
                           <img src="../../assets/img/_/paperprototype/negative_change_info.png" height="300 vh"> <br><br> 
                           <img src="../../assets/img/_/paperprototype/negative_change_info.png" height="300 vh"> <br><br> 
                           


                          
                            
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                            <h6>
                             AB Testing
                            </h6><br>
                            <p>
                              Conducting AB testing of paper prototypes helped to identify usability issues and refine the design of the app. This methodology allowed me to quickly test and iterate on different design concepts, ensuring that the final product is easy to use and visually appealing. 
                            </p>
                            
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                               Nasa tlx
                              </h6><br>
                              <p>
                                Using the NASA-TLX method helped to evaluate the overall cognitive load and mental effort required to use the app. This methodology allowed me to identify areas where the app may be overwhelming or confusing to users, and design solutions to reduce cognitive load and improve the overall user experience. By using the NASA-TLX method, I was able to ensure that the app is not only visually appealing and easy to use, but also efficient and effective in promoting healthy eating habits in the long run.
                              </p>
                              
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                             verbesserter prottoype
                              </h6><br>
                              <p>
                                Text 
                              </p>
                              <br>
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                               Unity prototype
                              </h6><br>
                              <p>
                                Text 
                              </p>
                              <br>
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                               usability Testing
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
                              </p>
                              <br>
        <br>
                       <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 
                        <br>
                              <h6>
                            retro / Conclusion
                              </h6><br>
                              <p>
                                Text 
                              </p>
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
                                Conducting a focus group allowed me to gather insights on the target audience's behavior and attitudes towards environmental impact. I was able to identify pain points and opportunities to motivate individuals to change their behavior using the augmented reality app.
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
                    </p>s
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
                         Based on the feedback from the paper prototype testing, an interactive prototype was developed using Unity. This prototype allowed users to experience the augmented reality app in a more realistic and immersive way, and provided valuable insights into how users interact with the app.
          
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

                      <br>  <br>
                          <h6>
                          Heuristic Evaluation
                          </h6><br>
                        <p>
                           A heuristic evaluation was conducted with 5 different individuals to identify usability issues and areas for improvement in the app. This evaluation helped to ensure that the app meets industry standards for usability and provided valuable insights into how to optimize the user experience. The Changes where mainly about the placing via AR in the World for a better imersive Experience.
                        </p>
                        <br> 


    <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 

     <br>  <br>
                            <h6>
                            Conclusion
                            </h6><br>
                          <p>
                             The development of this augmented reality app aimed at promoting positive environmental behavior has been a great success. Through the use of various UX design methods, it was able to create an app that is intuitive, engaging, and effective at motivating behavior change. The addition of features such as "My Garden" and the use of clear and concise language in the user interface has further enhanced the user experience.
                          </p>
                          <br> 


      <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br> 




    <br>  <br>
                            <h6>
                            Final Sources
                            </h6><br>
                          <p>
                             An full Impression of the Final Prototype you can see on my AR Tab on my Portfolio. 
                          </p>
                          <br> 
                           ----> See here the <a href="https://github.com/Michelle-P95/AR-virtual-Garden">Sourcecode on Github</a> of the final developed Prototype<br> 
                      
                  


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
                  

              
                <br><br>
                <p>First i conducted research and identified three primary user groups for the app. These personas served as a foundation for developing user-centered design solutions that meet the needs of both groups.</p>
  <br>
                <img src="../../assets/img/_/ux/Tattoo App - Persona 1.png" width="80%" style="display: block; margin: auto">
                <img src="../../assets/img/_/ux/Tattoo App - Persona 2.png" width="80%" style="display: block; margin: auto">
                <img src="../../assets/img/_/ux/Tattoo App - Persona 3.png" width="80%" style="display: block; margin: auto">
                <br>

                <p>To better understand the emotions, thoughts, and behaviors of our users, I created an empathy map. This helped me understand the users' needs and the barriers they face when seeking a tattoo artist. By using the empathy map, I was able to identify the users' pain points and develop solutions to overcome them.</p>
                
                <br>
                <img src="../../assets/img/_/ux/Tattoo App - Empathy Map.png" width="95%" style="display: block; margin: auto">
                <br>

                <p>To create a visual representation of the user's journey, I developed a storyboard. This helped me visualize the user's experience with the app from start to finish. By creating a storyboard, I was able to identify potential usability issues and design solutions to improve the user experience</p>

                <br>
                <img src="../../assets/img/_/ux/Tattoo App - Storyboard.png" width="80%" style="display: block; margin: auto">
                <br>

                <p>To create a seamless user experience, I developed a user flow that shows the user's path through the app. This user flow helped me identify areas of the app where the user may get lost or confused. By analyzing the user flow, I was able to make design decisions that guide the user and improve the overall experience.</p>
                
                <br>
                <img src="../../assets/img/_/ux/Tattoo App - User Flow.png" width="100%" style="display: block; margin: auto">
                <br>

                <p>In conclusion, the app design project involved employing several UX design methods, including personas, empathy maps, storyboards, and user flows. By using these methods, I was able to create a user-centered design that meets the needs of both first-time tattoo seekers and experienced tattoo enthusiasts. I believe that the app will provide a convenient and enjoyable experience for users seeking to find a suitable tattoo artist.</p>
    
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
  
                         <p>This is an Project about an App for displaying Dishes of a Menu in a Restaurant with Augmented Reality. Following you can see my Overview of my UX Process. </p>
  
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
    
                       
                        <img src="../../assets/img/_/text-info/arestaurant_info.png" style="display: block; margin: 0 auto; width: 85%;">
  <!--     ____      --><br><div style="border-bottom: 1px solid; color: black; width: 100%;"></div><br>
    <div class="description" style="color: black; font-size: 1.4em; text-decoration: underline; font-weight: bold;">Process</div>
                        <img src="../../assets/img/_/text-overview/overview_arestaurant.png" style="width: 50%">
                      <br>
                    
                    

                          !!! RETRO CONLUSCION - 
                
                
              
                 <br>
                

                <br>
                  <p>
                    To develop user personas, I conducted research and identified two primary user groups for the app.
                  </p>
                <br>

                <img src="../../assets/img/_/ux/ARestaurant - Persona 1.png" width="80%" style="display: block; margin: auto">
                  <img src="../../assets/img/_/ux/ARestaurant - Persona 2.png" width="80%" style="display: block; margin: auto">
              
                <br>
                    <p>
                      To create a visual representation of the user's journey, I developed a storyboard. This helped me visualize the user's experience with the app from start to finish. By creating a storyboard, I was able to identify potential usability issues and design solutions to improve the user experience.
                    </p>
                <br>
                
              
                <img src="../../assets/img/_/ux/ARestaurant - Storyboard.png" width="80%" style="display: block; margin: auto">
          
                    <br>
                      <p>
                        Below you can see a vidoe of the final implemented High Fidelity Prototype.
                      </p>
                  <br>
                  

                <br>
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
                  PROJECT 5
                </h3>
                <p class="date">
                  <a href="#"> </a>
                  Photoshop, Illustrator, InDesign <span>March 2022</span>
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

              <img src="../../assets/img/_/Design/PS.jpg" width="50%">

                <img src="../../assets/img/_/Design/Illustrator_Sign.png" width="50%"> <br><br>

                <img src="../../assets/img/_/Design/Mockup-Magazin.jpg">
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
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/Food4Me.png"),
          portfolioName: "AR App - Food4Me",
          //portfolioType: "AR",
          play: require("../../assets/img/_/play.png"),
          details: "made with User-Centered-Design in Unity3D.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/virtualGarden.png"),
          portfolioName: "AR App - virtual Garden",
          details: "made with User-Centered-Design in Unity3D.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/Handtracking.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/HandtrackingXR.png"),
          portfolioName: "XR / VR - Handtracking",
          //portfolioType: "XR",
           details: "made in Unity3D with Leapmotion, SteamVR",
          buttn: "",
        },
          {
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/ARestaurant.png"),
          portfolioName: "AR App - ARestaurant",
          //portfolioType: "AR",
          details: "made in Unity3D with Vuforia SDK.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/milka3.png"),
          portfolioName: "AR - Object Tracking",
           details: "made in Meta Spark Studio. can be used in Instagram.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/preview.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/neon-pink.png"),
          portfolioName: "AR - Glitch Art",
          details: "made in Lens Studio. experimental Glitch Art Filter.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/video_final_burger.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/burger.png"),
          portfolioName: "AR - Face Tracking",
           details: "made in Lens Studio. triggers with a kiss mouth.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/bubble_hat.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/bubble_hat.png"),
              portfolioName: "AR - Face Tracking",
                 details: "made in Lens Studio. triggers with open Mouth.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/YouVSWild.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/YouvsWild.png"),
              portfolioName: "AR - Face Tracking",
                  details: "made in Lens Studio. triggers with open Mouth Animations, Sounds and more.",
          buttn: "",
        },
        {
          src: require("../../assets/img/_/AR/video_conch.mp4"),
          autoplay: true,
          thumb: require("../../assets/img/_/AR/magic_conch.png"),
               portfolioName: "AR - Face Tracking",
                 details: "made in Lens Studio. Randomizer and triggers with Touch.",
          buttn: "",
        }
        
      
      ],
// ----------------------------------------------------------------------------- design      
      designItems: [
        {
          src: require("../../assets/img/_/Design/Illustrator_Sign.png"),
          thumb: require("../../assets/img/_/Design/Illustrator_Sign.png"),
          portfolioName: "(Illustrator)",
          portfolioType: "Design",
        },  
        {
          src: require("../../assets/img/_/Design/UX - Grafik - JobsToBeDone.jpg"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - JobsToBeDone.png"),
          portfolioName: "Jobs to be done",
          portfolioType: "Illustration",
        },
        {
          src: require("../../assets/img/_/Design/UX - Grafik - DesignMindset.jpg"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - DesignMindset.png"),
          portfolioName: "Design Thinking",
          portfolioType: "Illustration",
        },

        {
          src: require("../../assets/img/_/Design/UX Design - My Story.jpg"),
          thumb: require("../../assets/img/_/Design/UX Design - My Story.png"),
          portfolioName: "My UX learning Story",
          portfolioType: "Illustration",
        },
        {
          src: require("../../assets/img/_/Design/UX - Grafik - UXProcess Kopie.png"),
          thumb: require("../../assets/img/_/Design/UX - Grafik - UXProcess.png"),
          portfolioName: "UX-Process",
          portfolioType: "Illustration",
        },
        
      ],

// ----------------------------------------------------------------------------- 3D   
      dreiDItems: [
        {
          src: require("../../assets/img/_/3D/video-3d-game.mp4"),
            autoplay: true,
          thumb: require("../../assets/img/_/3D/mockup_3D-Game.png"),
          portfolioName: "(Unity)",
          portfolioType: "3D Game",
        }, 
        {
          src: require("../../assets/img/_/3D/video-3d-game.mp4"),
            autoplay: true,
          thumb: require("../../assets/img/_/3D/2D-Game.png"),
          portfolioName: "(Unity)",
          portfolioType: "2D Game",
        },
        {
          src: require("../../assets/img/_/3D/Bierkrug.jpg"),
          thumb: require("../../assets/img/_/3D/Bierkrug.png"),
          portfolioName: "(Maya)",
          portfolioType: "3D",
        },
        {
          src: require("../../assets/img/_/3D/taperecorder2.jpg"),
          thumb: require("../../assets/img/_/3D/taperecorder2.png"),
          portfolioName: "(Maya)",
          portfolioType: "3D",
        },
        {
          src: require("../../assets/img/_/3D/gameboy.png"),
          thumb: require("../../assets/img/_/3D/gameboy.png"),
          portfolioName: "(Blender)",
          portfolioType: "3D",
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

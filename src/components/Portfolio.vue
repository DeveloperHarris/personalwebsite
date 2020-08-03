<template>
  <div class="portfolio">
    <PortfolioItem
      v-for="item in portfolioItems"
      :key="item.title"
      :title="item.title"
      :image="item.image"
      :story="item.story"
    />
  </div>
</template>

<script>
import PortfolioItem from "./PortfolioItem.vue";

export default {
  name: "Portfolio",
  components: {
    PortfolioItem,
  },
  data() {
    return {
      portfolioItems: [
        {
          title: "Twitter Follower Export Tool",
          image: "pineapple.png",
          story:
            '<img src="https://user-images.githubusercontent.com/12452699/85966357-828c9500-b98d-11ea-9e47-d6028ef40320.gif"/>' +
            "<br/><br/>" +
            'Motivated by a bounty created by <a href="https://twitter.com/balajis/status/1272184608973447173">Balaji S. Srinivasan</a>, a friend and I created a Twitter Export CLI tool. Built with **Node**, its features include: ' +
            "<ul>" +
            "<li>Strong focus on locally stored information, no data stored online giving the user full control.</li>" +
            "<li>Intuitive and visually appealing CLI menu, allowing anyone to use it</li>" +
            "<li>Config file that stores Twitter API app keys allowing for a quick startup</li>" +
            "<li>Local SQLite database creating a seamless setup process</li>" +
            '<li>Ability to view all total followers and download or "sync" the information locally</li>' +
            "<li>Automatically handles API rate limits allowing a person to run once and forget</li>" +
            "<li>Export all downloaded follower information to CSV, with the option to only pick selected columns if preferred.</li>" +
            "<li>DM all followers w/ message preview and confirmation</li>" +
            "<li>DM test user w/ message preview and confirmation</li>" +
            "<li>Message parsing through handlebars.js allowing {id}, {screen_name}, {followers}, {friends} and other data to be used in messages for personalization</li>" +
            "<li>Reset config and followers database quickly through dedicated command</li>" +
            "</ul>" +
            "<br/>" +
            "Additionally, we also created desktop application designs and prototypes with **Oauth** & **Electron** but were unable to complete them in time for the bounty deadline." +
            "<br/><br/>" +
            '<img class="modalImages dropshadowImage" src="https://user-images.githubusercontent.com/12452699/85967509-a0a7c480-b990-11ea-94fc-ab9a0dba7410.png" width="75%"/>' +
            "<br/>" +
            'All the source code is available under an **MIT license** at : **<a href="https://github.com/DeveloperRyan/project-pineapple">Github Repo</a>**' +
            "<br/><br/>" +
            "Date: June 2020",
        },
        {
          title: "Calibur, Esports Startup",
          image: "darioharris.png",
          story:
            "Calibur was a startup founded in January 2019 by three undergraduate students (Dario Sujica, Bryan Becar & Harris Rothaermel) to create a LinkedIn for Esports." +
            "<br/><br/>" +
            "Calibur would be an online platform where users can create profiles containing personal, academic, and gaming information, which is then used to connect with esports organizations such as collegiate esports programs, and professional teams looking to recruit. These organizations would also have profiles that showcase their programs and can be found through a public directory." +
            "<br/><br/>" +
            '<iframe src="https://drive.google.com/file/d/12jql2MRKaRYvAxUuY0p8Im5H2DL_bQKn/preview" width="640" height="480"></iframe>' + // TODO: find better pdf imlpementation
            "<br/>" +
            "_Calibur - Key Pages_" +
            "<br/><br/>" +
            "We were fortunate to be one of the 16 companies selected to participate in BYU Rollins Center of Entrepreneurship Founder's Launchpad during the summer of 2019, where we participated in weekly lectures, reporting sessions, and hands-on mentorship. Soon after, we successfully raised **$40,000** of investments.  Our tech stack was comprised of **Angular/Django** for our initial scrimmage scheduling service, which had 200 teams use it during its public beta, and **React/Express** for our scholastic esports recruitment directory." +
            "<br/><br/>" +
            '<img class="modalImages" src="https://i.imgur.com/IrvovBz.jpg" width="50%"/>' +
            "<br/>" +
            "_BYU Founder's Launchpad - Summer 2019_" +
            "<br/><br/>" +
            "Due to the coronavirus pandemic and other factors, we were unable to raise additional capital, and in May of 2020 decided that it would be best for all involved to pack up and take our learnings to the next endeavor." +
            "<br/><br/>" +
            "Date: Jan 2019 - May 2020",
        },
        {
          title: "Web Programming Projects",
          image: "squak.png",
          story:
            "I created these projects as part of CS 260: Web Programming. We began the course by becoming well versed in pure **html & css**, and then progressed into **javascript**. I then took a detour and learned **React**, before rejoining the course schedule and learning **Vue**. We finished the course by becoming familiar with **Node, Express & MongoDB.**" +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab1.png" width="50%"/>' +
            "<br/>" +
            "Lab 1 - Photography Site" +
            "<br/>" +
            "_HTML / CSS_" +
            "<br/>" +
            '<a href="http://lab1.harrishr.xyz" target="_blank">Lab 1 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/creative1.jpg" width="50%"/>' +
            "<br/>" +
            "Creative Project 1 - API Design" +
            "<br/>" +
            "_HTML / CSS_" +
            "<br/>" +
            '<a href="http://creative1.harrishr.xyz" target="_blank">Creative Project 1 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab2.png" width="50%"/>' +
            "<br/>" +
            "Lab 2 - Weather Forecast" +
            "<br/>" +
            "_HTML / CSS / JS_" +
            "<br/>" +
            '<a href="http://lab2.harrishr.xyz" target="_blank">Lab 2 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/creative2.png" width="50%"/>' +
            "<br/>" +
            "Creative Project 2 - Game Stats" +
            "<br/>" +
            "_HTML / CSS / JS / React_" +
            "<br/>" +
            '<a href="http://creative2.harrishr.xyz" target="_blank">Creative Project 2 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab3a.png" width="50%"/>' +
            "<br/>" +
            "Lab 3a - XKCD Comic Browser" +
            "<br/>" +
            "_HTML / CSS / JS / Vue_" +
            "<br/>" +
            '<a href="http://lab3a.harrishr.xyz" target="_blank">Lab 3a Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/creative3.png" width="50%"/>' +
            "<br/>" +
            "Creative Project 3 - Twitter Clone" +
            "<br/>" +
            "_HTML / CSS / JS / Vue_" +
            "<br/>" +
            '<a href="http://creative3.harrishr.xyz" target="_blank">Creative Project 3 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab3b.png" width="50%"/>' +
            "<br/>" +
            "Lab 3b - Grocery Store" +
            "<br/>" +
            "_HTML / CSS / JS / Vue_" +
            "<br/>" +
            '<a href="http://lab3b.harrishr.xyz" target="_blank">Lab 3b Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/creative4.png" width="50%"/>' +
            "<br/>" +
            "Creative Project 4 - Esports Info" +
            "<br/>" +
            "_HTML / CSS / JS / Vue / MongoDB_" +
            "<br/>" +
            '<a href="http://creative4.harrishr.xyz" target="_blank">Creative Project 4 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab4.png" width="50%"/>' +
            "<br/>" +
            "Lab 4 - Image Upload" +
            "<br/>" +
            "_HTML / CSS / JS / Vue / MongoDB_" +
            "<br/>" +
            '<a href="http://lab4.harrishr.xyz" target="_blank">Lab 4 Link</a>' +
            "<br/><br/>" +
            '<img class="modalImages websiteImage" src="/static/lab5.jpg" width="50%"/>' +
            "<br/>" +
            "Lab 5 - Imgur Clone" +
            "<br/>" +
            "_HTML / CSS / JS / Vue / MongoDB_" +
            "<br/>" +
            '<a href="http://lab5.harrishr.xyz" target="_blank">Lab 5 Link</a>' +
            "<br/><br/>" +
            "Date: Jan 2020 - Apr 2020",
        },
        {
          title: "BYU HPT - Cubesat Payload",
          image: "PCS.jpg",
          story:
            " The payload’s guidance, navigation, and control system is comprised of an array of off-the-shelf and custom designed components. At its core is the Payload Control System (PCS) which is a 58mm x 110mm custom printed circuit board which features copper pads and traces for surface mount devices and components." +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/pcb.jpg" width="50%"/>' +
            "<br/>" +
            "_Payload Control System PCB_" +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/soldering.jpg" width="50%"/>' +
            "<br/>" +
            "_Soldering Components onto the Payload Control System (PCS)_" +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/pcs.jpg" width="50%"/>' +
            "<br/>" +
            "_Fully Assembled Payload Control System_" +
            "<br/><br/>" +
            "When assembled, the board features an Atmega 2560, an 8-bit microcontroller, and an extensive selection of sensors and peripherals for flight data collection. These sensors include the MPU-9250, a 9 axis inertial measurement unit, MPL115A2, a barometric pressure & temperature sensor, and the GP20U7, and a 56 channel GPS. By combining the data streams of these sensors, the payload’s exact location and attitude can be pinpointed." +
            "<br/><br/>" +
            "This data is stored locally through onboard flash memory, as well as a microSD card, which can be removed easily for post-flight analysis. In addition, the PCS features an XBee-PRO 900HP, a high powered transceiver which enables bidirectional radio communication up to a tested 5+ miles." +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/bootloading.jpg" width="50%"/>' +
            "<br/>" +
            "_Bootloading the Atmega using Arduino Uno_" +
            "<br/><br/>" +
            '<iframe width="500" height="300" src="https://www.youtube.com/embed/hqWCKJpesSk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/>" +
            "_How not to config a PID loop (outputs swapped)_" +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/recovery.jpg" width="50%"/>' +
            "<br/>" +
            "_Successful Recovery_" +
            "<br/><br/>" +
            "Recovery of the payload relies on two systems, the pyro channels on the PCS and an additional independently powered Stratologger CF for redundancy. When the payload is deployed, a quick-connect is broken and the PCS begins its programmed mission profile. One second after beginning it’s mission profile, the PCS fires the pyro channel associated with the drogue chute, and begins it’s coast phase. Once the payload reaches 4000 feet above ground level (AGL), the PCS deploys the main parachutes and initializes cold-gas thruster control." +
            "<br/><br/>" +
            "Power distribution is handled by two high-density lithium polymer (LiPo) batteries which were put in series to achieve 850mah of 14.8V - 16.4V. Lifetime calculations estimated that these batteries would power the payload for 1 hour and 12 minutes assuming the 7W solenoids, used for cold-gas thruster control, were powered 100% of the time." +
            "<br/><br/>" +
            "Date: Sept 2018 - Present",
        },
        {
          title: "BYU Rocketry",
          image: "MarkHarrisBYURocketryIREC.jpg",
          story:
            '<img class="modalImages" src="/static/teamPhoto.jpg" width="50%"/>' +
            "<br/>" +
            "_BYU High Powered Rocketry Team - 2019_" +
            "<br/><br/>" +
            "Being a member of BYU Rocketry has been one of the pinnacle experiences of my time at BYU. Since my freshman semester, I have learned how to design, model, and build rockets ranging from small model rockets to high powered compeition rockets. Additionally, I have had the opportunity to be a member on BYU Rocketry's High Powered Competition during the years of 2019, 2020 and 2021 as well as a member of the Hybrid Propulsion Research group. The experience and friendships I've made along the way are priceless, and I am extremely greatful such an organization exists at BYU. " +
            "<br/><br/>" +
            '<iframe width="500" height="300" src="https://www.youtube.com/embed/gcxcKwBVJCY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/>" +
            '_"Determination" - Launch Video_' +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/determination.jpg" width="50%"/>' +
            "<br/>" +
            '_"Determination" - Level 1 Certification Attempt_' +
            "<br/><br/>" +
            '<iframe width="500" height="300" src="https://www.youtube.com/embed/gsKepLebte8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/>" +
            '_"Stern" - Slowmo Launch Video_' +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/Stern.png" width="50%"/>' +
            "<br/>" +
            '_"Stern" - Freshman Lauch Competition Rocket_' +
            "<br/><br/>" +
            "Date: Sept 2017 - Present",
        },
        {
          title: "BYU Spacecraft Group",
          image: "femtosat.jpg",
          story:
            "The BYU Spacecraft Research Group is an organization at BYU that helps undergraduate students become spacecraft engineers. During my time there I had the opportunity to learn how to design, build, and program custom electronics, as well as learn the intricacies of RF and spacecraft operation. As part of the introductory freshamn comptetion, I created a femtosatellite which collected GPS, IMU, and barometric data, and then transmitted that data to a RF goundstation for post-processing." +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/femto.jpg" width="50%"/>' +
            "<br/>" +
            "_Femtosatellite PCB_" +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/assembly.jpg" width="50%"/>' +
            "<br/>" +
            "_PCB Assembly_" +
            "<br/><br/>" +
            '<img class="modalImages" src="/static/freshfemto.jpg" width="50%"/>' +
            "<br/>" +
            "_Fully Assembled Femtosatellite_" +
            "<br/><br/>" +
            "Date: Sept 2017 - Apr 2018",
        },
        {
          title: "Unreal Engine Renders",
          image: "unrealrender.jpg",
          story:
            '<iframe width="500px" height="300px" src="https://www.youtube.com/embed/YEAM70w4-Yw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/>" +
            '<iframe width="500px" height="300px" src="https://www.youtube.com/embed/RscgOcOuXUY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/>" +
            '<iframe width="500px" height="300px" src="https://www.youtube.com/embed/-jSpmZ4Zy_U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>' +
            "<br/><br/>" +
            "Date: May 2018 - August 2018",
        },
      ],
    };
  },
};
</script>

<style>
.portfolio {
  margin-top: 15px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-flow: row;
  flex-wrap: wrap;
  column-width: auto;
}

.websiteImage {
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);
}

@media screen and (max-width: 420px) {
  .modalImages {
    width: 100%;
  }

  iframe {
    width: 100%;
    height: 100%;
  }
}

ul {
  text-align: left;
}

.dropshadowImage {
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);
}
</style>

<script>
  import { selected } from "../stores/selected.store.js";
  import { fly, fade } from "svelte/transition";
</script>

<style>
  .flow-container {
    margin: 2vh auto;
    width: 80vw;
    min-height: 75vh;
    max-height: 85vh;
  }

  section {
    width: 100%;
    height: 100%;
    color: #333;
    max-height: 100%;
  }

  #skills {
    border-radius: 8px;
    text-align: center;
    background: hsl(184, 70%, 54%); /* fallback for old browsers */
    background: -webkit-linear-gradient(
      to right,
      #59bdeb,
      #95eff5
    ); /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(
      to right,
      #59bdeb,
      #95eff5
    ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  }

  #about {
    border-radius: 8px;
    background: #ee9ca7; /* fallback for old browsers */
    background: -webkit-linear-gradient(
      to left,
      #ffdde1,
      #ee9ca7
    ); /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(
      to left,
      #ffdde1,
      #ee9ca7
    ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  }

  #contact {
    border-radius: 8px;
    background: #1d976c; /* fallback for old browsers */
    background: -webkit-linear-gradient(
      to left,
      #93f9b9,
      #31e9a9
    ); /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(
      to left,
      #93f9b9,
      #31e9a9
    ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  }
</style>

<div class="clearfix" />
<div class="flow-container">
  {#if $selected == 'skills'}
    <section
      id="skills"
      in:fly={{ x: 200, duration: 500 }}
      out:fly={{ x: -200, duration: 500 }}>
      <div class="container">
        <div class="row">
          <div class="column">
            <p>
              As a Full Stack Web Dev, I'm familiar with a broad range of web
              technologies.
            </p>
            <h4>Front End</h4>
            <p>
              This includes JS frameworks such as AngularJS, Angular +
              Typescript & RxJS, and Svelte, CSS Frameworks such as Bootstrap
              and Milligram, and Modern CSS including Responsive Design,
              Flexbox, and CSS Grid.
            </p>
            <h4>Back End</h4>
            <p>
              I also have tons of experience utilizing back-end technologies
              such as Express, NestJS, MongoDB, and Mongoose. In addition, I
              also have proficiency using general purposes npm packages and JS
              libraries such as jQuery, momentJS, cheerio, uglify, multer, and
              much more!
            </p>
          </div>
        </div>
      </div>
    </section>
  {/if}
  {#if $selected == 'about'}
    <section
      id="about"
      in:fly={{ x: 200, duration: 500 }}
      out:fly={{ x: -200, duration: 500 }}>
      <div class="container">
        <!-- <div class="row">
      </div> -->
        <div class="row">
          <div class="column">
            <p>
              Hey! My name is Dan. I'm a professional Full Stack Web Developer
              living in Columbus, OH.
            </p>
            <p>
              I'm a huge tech enthusiast. I've built my own PCs and have helped
              several friends build their own PCs as well. I love playing video
              games in the few hours of spare time I have week. I mostly play
              Action RPGs and Shooters.
            </p>
            <p>
              I am also a music lover and muscian, I self-produced and released
              my own acoustic EP for free at spera.bandcamp.com. I listen to
              almost everything (truly!) but I love Post-Hardcore and
              Progressive Metal the most! I spent most of my free time nowadays
              playing guitar.
            </p>

            <p>
              I also tell jokes on twitter as @oxygenplug. Over the past four or
              five years I have built a following of over 7,000 followers. I
              have been featured in Playboy Humor, Mandatory, Thought Catalog,
              Buzzfeed, and the Chicago Tribune. I have also been a part of
              NASA's #NASAsocial program where I was invited to view and cover
              the launch of their MMS mission.
            </p>
            <p>
              Oh, also I stream video games from time to time at
              <a
                id="twitch-link"
                href="www.twitch.tv/oxygenplug"
                target="_blank">
                www.twitch.tv/oxygenplug
              </a>
            </p>
          </div>
        </div>
      </div>
    </section>
  {/if}
  {#if $selected == 'contact'}
    <section
      id="contact"
      in:fly={{ x: 200, duration: 500 }}
      out:fly={{ x: -200, duration: 500 }}>
      <h4>contact test</h4>
    </section>
  {/if}
</div>
<div class="clearfix" />

<script>
  import { selected } from "../stores/selected.store.js";
  import { fly, fade } from "svelte/transition";
</script>

<style>
  a {
    color: #fff;
    cursor: pointer;
  }
  section {
    width: 100%;
    height: 102%;
    color: #333;
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

  .headOne {
    grid-area: headOne;
  }

  .headTwo {
    grid-area: headTwo;
  }

  .bodyOne {
    grid-area: bodyOne;
  }

  .bodyTwo {
    grid-area: bodyTwo;
  }

  .full-center {
    position: relative;
    top: 5%;
    transform: translateY(-50%);
  }

  .title {
    font-size: 4em;
    letter-spacing: 1rem;
  }

  .body-text {
    font-size: 3rem;
  }

  .body-text > p {
    font-size: 2.35rem;
  }

  .flow-container {
    margin-left: 0;
    margin-right: 0;
    width: 100%;
  }

  .logo {
    color: #fff !important;
  }

  /* mobile screen */
  @media (min-width: 50px) {
    .grid-container {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 0.2fr 1fr 0.2fr 1fr;
      grid-template-areas: "headOne" "bodyOne" "headTwo" "bodyTwo";
    }
  }

  /* tablet screen */
  @media (min-width: 605px) {
    .grid-container {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 0.2fr 1fr 0.2fr 1fr;
      grid-template-areas: "headOne" "bodyOne" "headTwo" "bodyTwo";
    }
  }

  /* desktop screen */
  @media (min-width: 1100px) {
    .grid-container {
      display: grid;
      grid-template-columns: 0.5fr 1fr;
      grid-template-rows: 0.2fr 0.2fr;
      grid-template-areas: "headOne bodyOne" "headTwo bodyTwo";
      padding: 5px;
      height: 100%;
    }
    .flow-container {
      margin: 2vh auto;
      width: 80vw;
      min-height: 80vh;
    }

    #skills-grid {
      grid-row-gap: 15vh;
    }
  }
</style>

<div class="flow-container">
  {#if $selected == 'skills'}
    <section
      id="skills"
      in:fly={{ x: 200, duration: 500 }}
      out:fly={{ x: -200, duration: 500 }}>
      <div class="grid-container" id="skills-grid">
        <div class="headOne">
          <span class="full-center title">Front End</span>
        </div>
        <div class="headTwo">
          <span class="full-center title">Back End</span>
        </div>
        <div class="bodyOne">
          <span class="full-center body-text">
            JS frameworks such as AngularJS, Angular + Typescript & RxJS, and
            Svelte. CSS Frameworks such as Bootstrap and Milligram; Modern CSS
            including Responsive Design, Flexbox, and CSS Grid.
          </span>
        </div>
        <div class="bodyTwo">
          <span class="full-center body-text">
            I also have tons of experience utilizing back-end technologies such
            as Express, NestJS, MongoDB, and Mongoose. In addition, I also have
            proficiency using general purposes npm packages and JS libraries
            such as jQuery, momentJS, cheerio, uglify, multer, and much more!
          </span>
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
        <div class="row">
          <div class="column">
            <div class="grid-container">
              <div class="headOne">
                <span class="full-center title">Hey! My name is Dan.</span>
              </div>
              <div class="headTwo">
                <span class="full-center title" />
              </div>
              <div class="bodyOne">
                <span class="full-center body-text">
                  <p>
                    I'm a professional Full Stack Web Developer living in
                    Columbus, OH.
                  </p>
                  <p>
                    I'm a huge tech enthusiast. I've built my own PCs and have
                    helped several friends build their own PCs as well. I love
                    playing video games in the few hours of spare time I have
                    week. I mostly play Action RPGs and Shooters.
                  </p>
                  <p>
                    I am also a music lover and muscian, I self-produced and
                    released my own acoustic EP for free at spera.bandcamp.com.
                    I spent most of my free time nowadays playing guitar.
                  </p>
                </span>
              </div>
              <div class="bodyTwo">
                <span class="full-center body-text">

                  <p>
                    I also tell jokes on twitter as @oxygenplug. Over the past
                    four or five years I have built a following of over 7,000
                    followers. I have been featured in Playboy Humor, Mandatory,
                    Thought Catalog, Buzzfeed, and the Chicago Tribune. I have
                    also been a part of NASA's #NASAsocial program where I was
                    invited to view and cover the launch of their MMS mission.
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
                </span>
              </div>
            </div>
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
      <div class="container">
        <div class="row">
          <div class="column">
            <div class="row">
              <div class="column">
                <span class="full-center title">Want to get in touch?</span>
              </div>
            </div>
            <br />
            <div class="row">
              <div class="column column-50 column-offset-15">
                <h4>
                  <span>
                    <a href="mailto:dan.garces2@gmail.com">
                      <i class="fas fa-envelope logo" />
                    </a>
                    <strong>
                      <a href="mailto:dan.garces2@gmail.com">
                        dan.garces2@gmail.com
                      </a>
                    </strong>
                  </span>
                </h4>
              </div>
            </div>
            <br />
            <div class="row">
              <div class="column column-50 column-offset-15">
                <h4>
                  <span>
                    <a
                      target="_blank"
                      href="https://www.linkedin.com/in/dgarces2/">
                      <i class="fab fa-linkedin logo" />
                    </a>
                    <strong>
                      <a
                        target="_blank"
                        href="https://www.linkedin.com/in/dgarces2/">
                        LinkedIn
                      </a>
                    </strong>
                  </span>
                </h4>
              </div>
            </div>
            <br />
            <div class="row">
              <div class="column column-50 column-offset-15">
                <h4>
                  <span>
                    <a target="_blank" href="https://github.com/oxygenplug">
                      <i class="fab fa-github logo" />
                    </a>
                    <strong>
                      <a target="_blank" href="https://github.com/oxygenplug">
                        GitHub
                      </a>
                    </strong>
                  </span>
                </h4>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  {/if}
</div>
<div class="clearfix" />

<script>
  import { selected } from "../stores/selected.store.js";

  function updateSelection(val) {
    console.log("header val: ", val);
    selected.set(val);
  }
</script>

<style>
  * {
    font-size: 2.5rem;
  }

  #name {
    font-weight: 400;
    color: #333;
    text-align: center;
  }

  #mini-nav {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-evenly;
  }

  span {
    cursor: pointer;
  }

  .bottom-border {
    border-bottom: 3px solid #333;
  }

  .skills-class {
    color: #59bdeb;
  }

  .about-class {
    color: #ee9ca7;
  }
  .contact-class {
    color: #31e9a9;
  }

  #header {
    min-height: 9vh;
  }
</style>

<div class="container" id="header">
  <div class="row">
    <div class="column" id="name">D a n   G a r c e s</div>
  </div>
  <div class="row bottom-border">
    <div class="column" id="mini-nav">
      <span
        on:click={() => updateSelection('skills')}
        class:skills-class={$selected == 'skills'}>
        SKILLS
      </span>
      <span
        on:click={() => updateSelection('about')}
        class:about-class={$selected == 'about'}>
        ABOUT
      </span>
      <span
        on:click={() => updateSelection('contact')}
        class:contact-class={$selected == 'contact'}>
        CONTACT
      </span>
    </div>
  </div>
</div>
<div class="clearfix" />

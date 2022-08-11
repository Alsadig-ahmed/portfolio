<script>
  let openPopUp = false;
  export let showBtn = true;
</script>

<section>
  {#if showBtn}
    <div on:click={() => (openPopUp = !openPopUp)}><slot name="head" /></div>
  {/if}
  <div class:openPopUp class="popup">
    <span class="true"><div class="div" /></span>
    <div>
      <slot  name="content" >
        <h1>thank you</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam, quo.
          Consequuntur, dolore doloremque ad quaerat soluta eaque culpa.
        </p>
      </slot>
    </div>

    <button class="ok" on:click={() => (openPopUp = !openPopUp)}> ok </button>
  </div>
</section>

<style lang="scss">
  section {
    position: relative;
  }
  .ok {
    box-shadow: 0 0 1rem 0 grey;
  }
  .popup {
    background-color: rgb(243, 243, 243);
    text-align: center;
    min-width: 10rem;
    min-height: 5rem;
    max-width: max-content;
    border-radius: 2rem;
    padding: 0.5rem 1rem;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    $time: 500ms;
    transition: transform $time, left $time;
  }
  .openPopUp {
    box-shadow: 0 0 2rem 0 rgba(27, 27, 27, 0.774);
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .true {
    $h-w: 3rem;
    background-color: aliceblue;
    display: block;
    height: $h-w;
    width: $h-w;
    border-radius: 50%;
    text-align: center;
    margin: auto;
    margin-top: -2rem;
    padding: 0.3rem;
    box-shadow: 0 0 1rem 0 grey;
    position: relative;

    .div {
      position: absolute;
      top: 45%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-45deg);
      height: 1rem;
      width: 2.6rem;
      border: 5px solid greenyellow;
      border-right-width: 0;
      border-top-width: 0;
    }
  }
</style>

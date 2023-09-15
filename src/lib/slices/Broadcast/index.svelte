<script>
  /** @type {import("@prismicio/client").Content.BroadcastSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <div class="broadcast">
    <p>{slice.primary.broadcast}</p>
  </div>
</section>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
  }

  .broadcast {
    position: absolute;
    width: 100%;
    top: 0;
  }

  p {
    background-color: rgb(0, 0, 0);
    color: #ffffff;
    padding: 0.7rem;
    display: flex;
    justify-content: center;
  }

  @media screen and (max-width: 480px) {
      .broadcast {
    width: 150vw;
  }
  }
</style>

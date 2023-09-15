<script>
  /** @type {import("@prismicio/client").Content.MyClientsSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <div class="clients">
    <h2>{slice.primary.title}</h2>
    <img src={slice.primary.clients.url} alt="" />
  </div>
</section>

<style>
  h2 {
    display: flex;
    justify-content: center;
    padding-top: 6rem;
  }

  .clients {
    background-color: #3e55a1;
    background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/4273/circle-grid.svg);
    background-size: cover, 100px 100px;
    background-blend-mode: multiply;
  }

  @media screen and (max-width: 480px) {
      .clients {
    width: 150vw;
  }
  }
</style>

<script>
  /** @type {import("@prismicio/client").Content.MyWorkSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <div class="mywork" id="MyWork">
    <div class="website">
      <img src={slice.primary.website1.url} alt="" />
    </div>

    <div class="text">
      <h2>{slice.primary.title}</h2>
      <a
        href="https://wesleyschorel.github.io/What-color-is-this/"
        target="_blank">Visit Website</a
      >
    </div>
  </div>
</section>

<style>
  .mywork {
    background-color: #c5bae8;
    background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/4273/circle-grid.svg);
    background-size: cover, 100px 100px;
    background-blend-mode: multiply;
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    grid-template-rows: 1fr;
    grid-auto-columns: 1fr;
    gap: 0px 0px;
    grid-auto-flow: row;
    grid-template-areas: "avatar text";
  }

  .website {
    grid-area: avatar;
    padding: 3rem;
    display: flex;
    justify-content: center;
  }

  img {
    width: 100%;
    background: repeating-radial-gradient(
      100000px 10000px at 103000px 54000px,
      #ff5f9c 0 0.0001%,
      #fff 0 0.002%
    );
    box-shadow: 10px 10px 0px 0px #5c67af;
  }

  .text {
    margin-top: 5rem;
    grid-area: text;
    width: 80%;
  }

  @media screen and (max-width: 480px) {
      .mywork {
    width: 150vw;
  }
  }
</style>

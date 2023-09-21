<script>
  /** @type {import("@prismicio/client").Content.IntroSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <div class="intro">
    <div class="avatar">
      <img src={slice.primary.avatar.url} alt="" />
    </div>

    <div class="text">
      <h1>{slice.primary.title}</h1>
      <p><span>{slice.primary.text}</span></p>
      <p>{slice.primary.subtext}</p>
      <a href="/MyWork">My Work</a>
      <a href="/Contact">Contact</a>
    </div>
  </div>
</section>

<style>
  .intro {
    margin-top: 2rem;
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    grid-template-rows: 1fr;
    grid-auto-columns: 1fr;
    gap: 0px 0px;
    grid-auto-flow: row;
    grid-template-areas: "avatar text";
  }

  .avatar {
    grid-area: avatar;
    padding: 3rem;
    display: flex;
    justify-content: center;
  }

  img {
    border-radius: 50%;
    width: 40rem;
    background: repeating-radial-gradient(
      100000px 10000px at 103000px 54000px,
      #ff5f9c 0 0.0001%,
      #fff 0 0.002%
    );
    box-shadow: 10px 10px 0px 0px #ff5f9c;
  }

  .text {
    margin-top: 5rem;
    grid-area: text;
    width: 80%;
  }

  @media screen and (max-width: 480px) {
    .intro {
      display: grid;
      grid-auto-columns: 1fr;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;
      gap: 0px 0px;
      grid-template-areas:
        "text"
        "avatar";

      padding: 2rem;
    }

    img {
    border-radius: 50%;
    width: auto;
    height: 30rem;
    background: repeating-radial-gradient(100000px 10000px at 103000px 54000px, #ff5f9c 0 0.0001%, #fff 0 0.002%);
    box-shadow: 10px 10px 0px 0px #ff5f9c;
  }

  .text {
    margin-top: 5rem;
    grid-area: text;
    width: 80%;
  }
  }
</style>


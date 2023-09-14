<script>
  /** @type {import("@prismicio/client").Content.IntroSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <div class="avatar">
   <img src={slice.primary.avatar.url} alt="" />
  </div>

  <div class="text">
    <h1>{slice.primary.title}</h1>
    <p>{slice.primary.text}</p>
    <p>{slice.primary.subtext}</p>
    <a href="/MyWork">My Work</a>
    <a href="/Contact">Contact</a>
  </div>

</section>


<style>
section {  display: grid;
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
  width: 80%;;
  background: repeating-radial-gradient(100000px 10000px at 103000px 54000px,#000 0 .0001%,#fff 0 0.002%);
  box-shadow: 10px 10px 0px 0px rgba(210,104,104,1);
}

.text { 
  grid-area: text;
  width: 80%;
}
</style>
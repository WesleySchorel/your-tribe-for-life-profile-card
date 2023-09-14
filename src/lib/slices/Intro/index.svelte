<script>
  /** @type {import("@prismicio/client").Content.IntroSlice} */
  export let slice;
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
<h1>{slice.primary.title}</h1>
<p>{slice.primary.text}</p>
</section>

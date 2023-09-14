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
}
</style>
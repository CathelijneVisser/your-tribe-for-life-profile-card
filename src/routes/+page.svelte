
<script>
  import { SliceZone } from '@prismicio/svelte'
  import { components } from '$lib/slices'
  export let data

</script>


<section>

<h1>{data.slices[0].primary.name}</h1>
<img src="{data.slices[0].primary.picture}">

</section>

 

 
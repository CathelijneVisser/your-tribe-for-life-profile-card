
<script>
  import { SliceZone } from '@prismicio/svelte'
  import { components } from '$lib/slices'
  export let data

</script>


<section>
<!-- {#each data.items as item }
    <p>{item.text}</p>
{/each} -->
  <!-- <h1>{data.name[0].text}</h1> -->
<p>{data.slices[0].primary.name}</p>

  <hr>  

  <SliceZone slices={data.slices} {components} />
  <pre>

Data uit prismic:

 

{JSON.stringify(data, null, 2)}

  </pre>

</section>

 

 
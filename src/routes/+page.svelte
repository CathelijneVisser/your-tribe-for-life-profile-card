
<script>
  import { SliceZone } from '@prismicio/svelte'
  import { components } from '$lib/slices'
  export let data
</script>
<SliceZone slices={data.slices} {components} />

<section>

<h1>{data.slices[0].primary.name}</h1>
<img src="{data.slices[0].primary.picture.url}">


</section>

<section>
    <p>Hoi Ik ben Cathelijne, ik ben 
      {data.slices[0].primary.age} jaar.
    </p>
</section>
 
<section>
  <p>
    Mijn hobby's zijn:
    {data.slices[0].primary.hobbys[0].text}.

  </p>
  </section>

  <!-- <pre>
{JSON.stringify(data, null, 2)}

  </pre> -->



<style>
    body{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    section{
        border: 2px solid black;
        width: 10em;
        height: 10em;
        padding: 1em;
        margin: 1em;
    }

    section:first-of-type {
      display: flex;
      flex-direction: column;

    }

    h1 {
      margin: 0;
      font-size: 1em;
    }

    img {
      width: 5em;
      margin-top: 1em;
    }
</style>
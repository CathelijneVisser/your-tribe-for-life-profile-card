<script>
  import * as prismic from "@prismicio/client";
  import { SliceZone } from "@prismicio/svelte";
  import { components } from "$lib/slices";
  export let data;
</script>

<section>
  <h1>{data.name}</h1>
  <img src={data.picture.url} alt="" />
</section>

<section>
  <p>
    Hoi Ik ben Cathelijne, ik ben
    {data.age} jaar. Mijn hobby's zijn:
    {data.hobbys[0].text}.
  </p>
</section>

<section>
  <a href={data.github.url}>Mijn github kun je hier vinden.</a>
  <a href={data.linkedin.url}>Mijn linkedin kun je hier vinden.</a>
  <p>Mijn email adress is {data.email[0].text}</p>

</section>

<SliceZone slices={data.slices} {components} />

<!-- <pre>
{JSON.stringify(data, null, 2)}
  </pre> -->

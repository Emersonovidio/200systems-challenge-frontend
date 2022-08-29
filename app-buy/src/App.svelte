<script>
  import Buy from "./buttom.svelte";

  let name = "";
  let product = "";
  let promocode = "";
  function setTitle(event) {
    name = event.target.value;
  }
  let thisname = "products";
</script>

<svelte:head>
  <title>Indications Program</title>
  <meta name="robots" content="noindex nofollow" />
  <html lang="en" />
</svelte:head>

<h1>Buy our awesome {thisname} !!</h1>

<hr />
<section>
  <div>
    <label for="title">Your Name</label>
    <input type="text" id="title" value={name} on:input={setTitle} />
  </div>
  <div>
    <label for="product">Product Name</label>
    <input type="text" id="product" value={product} on:input={product} />
  </div>
  <div>
    <label for="promocode">My promo code</label>
    <textarea rows="3" id="promocode" bind:value={promocode} />

    <Buy nameTitle={name} nameProduct={product} nameDescription={promocode} />
  </div>
</section>

<style>
  section {
    margin: 75px;
    width: 50rem;
    font-size: large;
  }

  h1 {
    font-size: xx-large;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
      "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    margin-top: 25px;
  }
  
</style>

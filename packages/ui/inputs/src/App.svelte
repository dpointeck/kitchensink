<script lang="ts">
  import Input from "./lib/Input.svelte";
  import TextArea from "./lib/TextArea.svelte";
  let name = "";
  let age = "";
  let time = "";
</script>

<main>
  <label for="name">
    <span>Name</span>
    <Input id="name" name="name" type="text" bind:value={name} />
  </label>
  {name}
  <Input type="number" bind:value={age} />
  {age}
  <Input type="password" bind:value={age} />

  <Input type="time" bind:value={time} />

  <TextArea id="bio" name="bio" cols="20" rows="5" />
</main>

<style>
  main {
    display: grid;
    justify-content: start;
    gap: 16px;
    padding: 1em;
    max-width: 360px;
    margin: 0 auto;
  }
  label > span {
    text-align: left;
  }
</style>

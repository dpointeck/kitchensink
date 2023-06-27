<script lang="ts">
  import { Input } from 'ui';

  let name = '';
</script>

<main class="">
  <label for="name">Name</label>
  <Input bind:value={name} />
  { name }
</main>


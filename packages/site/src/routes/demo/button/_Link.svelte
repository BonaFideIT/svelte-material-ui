<Button onclick={() => clicked++} href="http://example.com" target="_blank">
  <Label>Link</Label>
</Button>

<pre class="status">Clicked: {clicked}</pre>

<script lang="ts">
  import Button, { Label } from '@smui/button';

  let clicked = $state(0);
</script>

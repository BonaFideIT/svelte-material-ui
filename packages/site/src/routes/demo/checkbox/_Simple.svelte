<div>
  <FormField>
    <Checkbox bind:checked />
    {#snippet label()}
      Remember me.
    {/snippet}
  </FormField>
</div>

<pre class="status">Checked: {checked}</pre>

<div style="margin-top: 1em;">
  <FormField align="end">
    <Checkbox bind:checked={checked2} />
    {#snippet label()}
      Remember me.
    {/snippet}
  </FormField>
</div>

<div style="margin-top: 1em;">
  <Button onclick={() => (checked2 = !checked2)}>
    Toggle Programmatically
  </Button>
</div>

<pre class="status">Checked: {checked2}</pre>

<script lang="ts">
  import Checkbox from '@smui/checkbox';
  import FormField from '@smui/form-field';
  import Button from '@smui/button';

  let checked = $state(false);
  let checked2 = $state(false);
</script>

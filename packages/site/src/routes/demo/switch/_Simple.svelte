<div>
  <FormField>
    <Switch bind:checked={checked1} />
    {#snippet label()}
      Fields of grain.
    {/snippet}
  </FormField>
</div>

<pre class="status">Checked: {checked1}</pre>

<div style="margin-top: 1em;">
  <FormField align="end">
    <Switch bind:checked={checked2} />
    {#snippet label()}
      Fields of grain.
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
  import Switch from '@smui/switch';
  import FormField from '@smui/form-field';
  import Button from '@smui/button';

  let checked1 = $state(false);
  let checked2 = $state(false);
</script>

<Set chips={choices} choice bind:selected>
  {#snippet chip(chip)}
    <Chip {chip}>
      <Text>{chip}</Text>
    </Chip>
  {/snippet}
</Set>

<div style="margin-top: 1em;">Programmatically select:</div>
<Button onclick={() => (selected = 'Morning')}>
  <Label>Morning</Label>
</Button>
<Button onclick={() => (selected = 'Afternoon')}>
  <Label>Afternoon</Label>
</Button>
<Button onclick={() => (selected = 'Evening')}>
  <Label>Evening</Label>
</Button>
<Button onclick={() => (selected = 'Night')}>
  <Label>Night</Label>
</Button>

<pre class="status">Selected: {selected}</pre>

<script lang="ts">
  import Chip, { Set, Text } from '@smui/chips';
  import Button, { Label } from '@smui/button';

  let choices = ['Morning', 'Afternoon', 'Evening', 'Night'];
  let selected = $state('Morning');
</script>

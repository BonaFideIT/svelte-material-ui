<div style="display: flex; align-items: center;">
  <IconButton onclick={() => clicked++}>
    <Icon tag="svg" viewBox="0 0 24 24">
      <path fill="currentColor" d={mdiFormatColorFill} />
    </Icon>
  </IconButton>
</div>
<div style="display: flex; align-items: center;">
  <IconButton onclick={() => clicked++} disabled>
    <Icon tag="svg" viewBox="0 0 24 24">
      <path fill="currentColor" d={mdiWrench} />
    </Icon>
  </IconButton>&nbsp;(disabled)
</div>
<div style="display: flex; align-items: center;">
  <IconButton onclick={() => clicked++} ripple={false}>
    <Icon tag="svg" viewBox="0 0 24 24">
      <path fill="currentColor" d={mdiCurrencyUsd} />
    </Icon>
  </IconButton>&nbsp;(no ripple)
</div>

<pre class="status">Clicked: {clicked}</pre>

<script lang="ts">
  import { mdiFormatColorFill, mdiWrench, mdiCurrencyUsd } from '@mdi/js';
  import IconButton, { Icon } from '@smui/icon-button';

  let clicked = $state(0);
</script>

<div class="columns margins">
  <div>
    <Textfield
      bind:value={valueA}
      label="Standard"
      prefix="$"
      input$pattern={'\\d+(\\.\\d{2})?'}
    />

    <pre class="status">Value: {valueA}</pre>
  </div>
  <div>
    <Textfield
      variant="filled"
      bind:value={valueB}
      label="Filled"
      prefix="$"
      input$pattern={'\\d+(\\.\\d{2})?'}
    />

    <pre class="status">Value: {valueB}</pre>
  </div>
  <div>
    <Textfield
      variant="outlined"
      bind:value={valueC}
      label="Outlined"
      prefix="$"
      input$pattern={'\\d+(\\.\\d{2})?'}
    />

    <pre class="status">Value: {valueC}</pre>
  </div>
</div>

<script lang="ts">
  import Textfield from '@smui/textfield';

  let valueA = $state('');
  let valueB = $state('');
  let valueC = $state('');
</script>

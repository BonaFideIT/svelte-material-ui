<div class="margins">
  <!--
    Note: when you bind to `invalid`, but you only want to
    monitor it instead of updating it yourself, you also
    should include `updateInvalid`.
  -->
  <Textfield
    type="email"
    bind:dirty
    bind:invalid
    updateInvalid
    bind:value
    label="To"
    style="min-width: 250px;"
    input$autocomplete="email"
    onfocus={() => (focused = true)}
    onblur={() => (focused = false)}
    withTrailingIcon={!disabled}
  >
    <!--
      Since this icon is conditional, it needs to be wrapped
      in a fragment, and we need to provide withTrailingIcon.
    -->
    {#snippet trailingIcon()}
      {#if !disabled}
        <Icon class="material-icons" role="button" onclick={clickHandler}
          >send</Icon
        >
      {/if}
    {/snippet}
    {#snippet helper()}
      <HelperText validationMsg>That's not a valid email address.</HelperText>
    {/snippet}
  </Textfield>
</div>

<pre
  class="status">Focused: {focused}, Dirty: {dirty}, Invalid: {invalid}, Value: {value}</pre>

<script lang="ts">
  import Textfield from '@smui/textfield';
  import Icon from '@smui/textfield/icon';
  import HelperText from '@smui/textfield/helper-text';

  let focused = $state(false);
  let value: string | null = $state(null);
  let dirty = $state(false);
  let invalid = $state(false);
  const disabled = $derived(focused || !value || !dirty || invalid);

  function clickHandler() {
    alert(`Sending to ${value}!`);
    value = null;
    dirty = false;
  }
</script>

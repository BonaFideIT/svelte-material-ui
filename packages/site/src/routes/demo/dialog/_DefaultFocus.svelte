<Dialog
  bind:open
  aria-labelledby="default-focus-title"
  aria-describedby="default-focus-content"
>
  <Title id="default-focus-title">Advice</Title>
  <Content id="default-focus-content">
    Build something today, even if it sucks.
  </Content>
  <Actions>
    <Button onclick={() => (response = 'I will make you! Do it!')}>
      <Label>You Can't Make Me</Label>
    </Button>
    <Button
      defaultAction
      use={[InitialFocus]}
      onclick={() => (response = 'It will be glorious.')}
    >
      <Label>I Will</Label>
    </Button>
  </Actions>
</Dialog>

<Button onclick={() => (open = true)}>
  <Label>Open Dialog</Label>
</Button>

<pre class="status">Response: {response}</pre>

<script lang="ts">
  import Dialog, { Title, Content, Actions, InitialFocus } from '@smui/dialog';
  import Button, { Label } from '@smui/button';

  let open = $state(false);
  let response = $state('Nothing yet.');
</script>

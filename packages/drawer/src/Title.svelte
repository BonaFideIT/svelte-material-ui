<svelte:options runes />

<ClassAdder
  _smuiClass="mdc-drawer__title"
  tag="h1"
  bind:this={element as ReturnType<C>}
  {...restProps}>{@render children?.()}</ClassAdder
>

<script
  lang="ts"
  generics="T extends SmuiEveryElement = keyof SmuiElementPropMap, C extends SmuiComponent = SmuiComponent"
>
  import type { ComponentProps, Snippet } from 'svelte';
  import type {
    SmuiComponent,
    SmuiElementPropMap,
    SmuiEveryElement,
  } from '@smui/common';
  import { ClassAdder } from '@smui/common/classadder';

  type OwnProps = {
    children?: Snippet;
  };
  let { children, ...restProps }: OwnProps & ComponentProps<ClassAdder<T, C>> =
    $props();

  let element: ReturnType<C>;

  export function getElement() {
    return element.getElement();
  }
</script>

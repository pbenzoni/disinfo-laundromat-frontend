<script lang="ts">
  import { cn } from '$utils';
  export let ariaLabel: string;
  export let onClick: () => void = () => {};
  let className: string | undefined = undefined;
  export { className as class };
</script>

<button
  on:click={onClick}
  aria-label={ariaLabel}
  class={cn(
    'rounded-input text-background shadow-mini hover:bg-dark/95 active:scale-98 inline-flex h-12 items-center justify-center bg-white px-[21px] text-[15px] font-semibold active:transition-all',
    className
  )}
  {...$$restProps}
>
  <slot />
</button>

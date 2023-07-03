<script lang="ts">
  import { createStyles } from "@svelteuidev/core";

  interface ButtonProps {
    color: "blue" | "violet";
    radius: number;
  }

  let color: ButtonProps["color"] = "blue";
  let radius: ButtonProps["radius"] = 50;

  const useStyles = createStyles(
    (theme: any, { color, radius }: ButtonProps) => {
      return {
        root: {
          color: 'white',
          backgroundColor: theme.fn.themeColor(color, 6),
          borderRadius: radius,
          padding: '$mdPX',
          margin: '$mdPX',
          border: 0,
          cursor: 'pointer',
        },
      };
    }
  );

  // This is reactive destructuring
  $: ({ getStyles } = useStyles({color, radius}));

  console.log(getStyles);
</script>

<button type="button" class={getStyles()}>
  {color} button with radius {radius}px
</button>


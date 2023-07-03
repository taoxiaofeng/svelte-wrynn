<script>
	import { keyframes, Button } from '@svelteuidev/core';

	const scaleUp = keyframes({
		'0%': { transform: 'scale(1)' },
		'100%': { transform: 'scale(1.5)' }
	});

	const styles = {
		'&:hover': {
			animation: `${scaleUp} 200ms`
		}
	};
</script>

<Button override={styles}>I will grow on hover</Button>
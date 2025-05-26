<script lang="ts">
	import { animate, stagger, svg } from 'animejs';
import { onMount } from 'svelte';

onMount(() => {
  // First ensure anime.js is loaded from CDN
      
      // Set CSS variable for each path to create staggered animation
      
      // Use anime.js to animate each path - only animate the stroke, not the fill
      const pathAnimation = animate(svg.createDrawable('.svg-path'), {
		draw: ['0 0', '0 1', '1 1'],
		ease: 'easeInOutSine',
		duration: 3000,
		delay: stagger(100), // Stagger the animation of each path
		loop: true, // Only draw once
      });

      // Apply the no-fill class to the d and last a in "villla"
      // The 4th path is the 'd' in villla, and the last path (18th) is the final 'a'
      const pathElements = document.querySelectorAll('.svg-path');
      // "d" letter in villla - 4th letter
      if (pathElements[3]) pathElements[3].classList.add('no-fill');
      // Last "a" in villla - the last path with the rounded pocket
      if (pathElements[17]) pathElements[17].classList.add('no-fill');
      
}
)

</script>

<main class="w-screen h-screen p-24 pt-16 grid place-items-center select-none bg-background">
	<div>
			<!-- Using the SVG directly -->
			<svg width="800" height="100" viewBox="0 0 365 51" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
				<g filter="url(#filter0_d_2_4)">
					<path class="svg-path" d="M40.608 17.344L33.504 22.592L21.856 47.936L21.792 47.872L20.512 50.752L7.456 22.336L0.863998 17.344H20.064L15.648 20.992L22.944 38.208L30.112 21.888L25.888 17.344H32.032V17.536L32.096 17.344H40.608Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M39.036 48L43.644 43.52V25.28L39.036 22.912L43.644 20.096L47.42 17.792L51.324 15.424V43.52L56.252 48H39.036Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M43.004 7.04C43.004 4.416 45.18 2.176 47.868 2.176C50.492 2.176 52.732 4.416 52.732 7.04C52.732 9.728 50.492 11.904 47.868 11.904C45.18 11.904 43.004 9.728 43.004 7.04Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M73.576 48.832C66.728 48.832 59.624 43.968 59.624 33.344C59.624 24.768 66.856 16.832 77.352 16.832C79.144 16.832 81.128 17.152 83.048 17.92V10.432L78.44 8.192L88.424 1.536V1.6L90.728 -3.8147e-06V41.088L95.336 44.288L84.968 49.472L83.432 43.968C81.256 47.36 77.16 48.832 73.576 48.832Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M77.864 43.136C79.144 43.136 81.256 43.008 83.048 41.664V27.2C82.6 22.336 80.104 20.032 76.008 20.032C70.824 20.032 67.56 24.576 67.56 30.4C67.56 39.04 72.168 43.136 77.864 43.136Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M116.209 21.312C111.665 21.312 110.257 24.768 109.873 26.56V43.52L114.865 48H97.585L102.257 43.456V10.432L97.649 8.192L109.937 -3.8147e-06L109.873 21.44C111.921 18.432 114.865 16.704 119.473 16.704C125.553 16.704 129.841 20.544 129.841 27.84L129.777 43.52L134.769 48H117.489L122.097 43.52L122.161 29.76C122.161 26.368 121.969 24.896 121.009 23.424C120.113 22.016 118.513 21.312 116.209 21.312Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M167.695 15.424V41.088L172.303 44.288L161.935 49.472L160.463 43.328C158.479 46.72 155.663 48.704 150.735 48.704C144.655 48.704 140.495 44.864 140.495 37.568V25.216L135.951 22.912L144.335 17.792V17.856L148.239 15.424L148.175 35.264C148.239 40.64 149.391 43.968 154.127 43.968C158.415 43.968 159.631 40.96 160.015 39.168V25.28L155.407 22.912L163.791 17.792V17.856L167.695 15.424Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M181.627 14.208C181.627 12.608 180.411 11.968 179.899 11.904C179.259 11.52 176.763 10.56 176.763 7.104C176.763 4.352 178.939 1.984 182.203 1.984C185.019 1.984 187.899 4.608 187.899 9.024C187.899 16.576 181.371 21.504 179.771 22.528C178.939 22.976 178.235 22.784 178.107 22.592C177.979 22.336 177.979 21.824 178.299 21.44C179.387 19.968 181.627 17.408 181.627 14.208Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M203.765 16.384C205.941 16.384 208.373 17.216 210.037 18.176L215.029 15.424L215.093 28.544C213.685 25.984 212.085 23.744 209.717 21.888C208.245 20.608 205.941 19.84 204.213 19.84C201.141 19.84 198.901 21.184 198.901 23.68C198.901 25.664 201.397 26.88 205.237 27.84C211.893 29.504 216.181 31.488 216.181 38.784C216.181 43.072 212.789 48.64 205.493 48.64C202.165 48.64 199.797 47.808 198.005 46.784L193.205 49.152L193.141 34.88C195.189 38.016 196.917 41.28 199.797 43.52C201.589 44.864 203.317 45.12 205.621 45.12C207.733 45.12 210.421 43.84 210.421 41.216C210.421 37.568 206.005 36.8 202.997 36.16C196.981 34.88 193.269 32.32 193.269 26.048C193.269 19.776 198.133 16.384 203.765 16.384Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M275.171 17.344L268.067 22.592L256.419 47.936L256.355 47.872L255.075 50.752L242.019 22.336L235.426 17.344H254.627L250.211 20.992L257.507 38.208L264.675 21.888L260.451 17.344H266.595V17.536L266.659 17.344H275.171Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M273.599 48L278.207 43.52V25.28L273.599 22.912L278.207 20.096L281.983 17.792L285.887 15.424V43.52L290.815 48H273.599Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M277.567 7.04C277.567 4.416 279.743 2.176 282.431 2.176C285.055 2.176 287.295 4.416 287.295 7.04C287.295 9.728 285.055 11.904 282.431 11.904C279.743 11.904 277.567 9.728 277.567 7.04Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M292.843 48L297.515 43.456V10.432L292.907 8.192L305.195 -3.8147e-06L305.131 43.52L310.123 48H292.843Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M312.53 48L317.202 43.456V10.432L312.594 8.192L324.882 -3.8147e-06L324.818 43.52L329.81 48H312.53Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M352.186 26.176H352.25C351.994 21.824 349.178 19.456 345.978 19.456C344.058 19.456 341.05 19.84 340.154 21.12C342.906 22.208 343.61 23.808 343.61 25.984C343.61 28.48 341.498 30.464 339.194 30.464C336.378 30.464 334.842 28.224 334.842 25.28C334.842 21.504 340.474 16.384 347.066 16.384H348.09C353.658 16.384 359.546 18.944 359.546 27.52C359.546 30.144 359.482 40 359.482 42.944L364.346 48H353.85L352.25 43.072C350.266 46.528 345.85 48.896 341.626 48.896C335.674 48.896 333.818 44.48 333.818 41.6C333.818 37.12 337.594 34.496 341.562 33.536C346.17 32.448 352.25 31.744 352.186 26.176Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
					<path class="svg-path" d="M344.698 44.096C347.002 44.096 350.65 42.688 352.058 39.296L352.186 31.552C350.65 33.536 348.282 34.752 346.17 35.584C342.714 37.12 341.434 38.592 341.434 41.024C341.434 42.944 343.034 44.096 344.698 44.096Z" stroke="var(--color-foreground)" fill="var(--color-muted)" />
				</g>
			</svg>
		</div>
</main>

<style>
	.logo-container {
		margin-top: -50px;
	}
	
	.svg-path {
		stroke-width: 2;
		stroke-linecap: round;
		stroke-linejoin: round;
		fill-opacity: 0.5; /* Always show fill with partial opacity */
	}
	
	/* Remove fill from specific letters ('d' and last 'a' in "villla") */
	.svg-path.no-fill {
		fill-opacity: 0 !important; /* Override any other fill opacity settings */
	}
	
	/* Animate the stroke of the path */
	.svg-path {
		stroke-opacity: 0;
		animation: fadeInStroke 0.3s ease-in-out forwards;
		animation-delay: calc(var(--index, 0) * 100ms); /* Delay based on path index */
	}
	
	@keyframes fadeInStroke {
		from { stroke-opacity: 0; }
		to { stroke-opacity: 1; }
	}
	
	/* When the stroke animation is done, boost the fill opacity slightly */
	.svg-path.animated {
		fill-opacity: 0.8;
		transition: fill-opacity 0.5s ease-in-out;
	}
</style>
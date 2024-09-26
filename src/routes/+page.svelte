<script>
	import gsap from 'gsap';

	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		const screen1 = gsap.timeline({
			scrollTrigger: {
				trigger: '.section-1', // Trigger animation on this section
				start: 'top top', // Start when the top of the section hits the top of the viewport
				end: 'bottom top', // End when the bottom of the section hits the top of the viewport
				markers: true,
				scrub: true
			}
		});

		gsap.fromTo(
			'.section-1 .section-1__bg',
			{ opacity: 0.1, y: 50 },
			{
				opacity: 0.25,
				y: 0,
				duration: 5,
				scale: 1.2
			}
		);

		gsap.fromTo(
			'.section-1 .section__title',
			{ opacity: 0.1, scale: 0 },
			{ opacity: 1, scale: 1, duration: 0.5 } // Final state
		);

		screen1.fromTo(
			'.section-1 .section__subtitle',
			{ opacity: 0, y: 30 },
			{ opacity: 1, y: 0, duration: 1 },
			'-=0.5' // Start this animation 0.5 seconds before the title animation ends
		);

		gsap.fromTo(
			'.section-2 .section-2__bg',
			{ opacity: 0.1, scale: 1 },
			{
				opacity: 0.25,
				duration: 5,
				scale: 1.8,
				scrollTrigger: {
					trigger: '.section-2', // Trigger animation on this section
					start: 'top center', // Start when the top of the section hits the top of the viewport
					end: 'bottom center',
					markers: true
				}
			}
		);

		gsap.fromTo(
			'.section-2 .section__title',
			{ opacity: 0.1, scale: 0 },
			{
				opacity: 1,
				scale: 1,
				duration: 0.5,
				scrollTrigger: {
					trigger: '.section-2', // Trigger animation on this section
					start: 'top center', // Start when the top of the section hits the top of the viewport
					end: 'bottom center',
					markers: true
				}
			} // Final state
		);

		const screen2 = gsap.timeline({
			scrollTrigger: {
				trigger: '.section-2', // Trigger animation on this section
				start: 'top center', // Start when the top of the section hits the top of the viewport
				end: 'bottom center',
				markers: true,
				scrub: true
			}
		});

		screen2.fromTo('.section-2 .section__subtitle', { opacity: 0 }, { opacity: 1 }).fromTo(
			'.section-2 .section-2__person',
			{ opacity: 0 }, // Initial state
			{
				duration: 1,
				opacity: 0.95
			}
		);
	});
</script>

<div class="section section-1">
	<div class="section-1__bg"></div>
	<div class="section__body">
		<h1 class="section__title">
			<span class="text-accent">Empowering</span> Your Vision with Full-Stack
			<span class="expertise">Expertise</span>
		</h1>
		<p class="section__subtitle">
			Leveraging cutting-edge technologies to craft dynamic, end-to-end web solutions tailored to
			your unique goals.
		</p>
	</div>
</div>
<div class="section section-2">
	<div class="section-2__person"></div>
	<div class="section-2__bg"></div>
	<div class="section__body">
		<h1 class="section__title">
			Hello <span class="text-accent">World! Im Dave</span>
		</h1>
		<p class="section__subtitle subtitle-2">
			Armed with a diverse skill sets, I breathe life into digital ideas and transform them into
			functional realities.
		</p>
        <div class="logos">
            <div class="svelte"></div>
            <div class="javascript"></div>
            <div class="css"></div>
            <div class="node"></div>
            <div class="react"></div>
            <div class="vue"></div>
            <div class="php"></div>
            <div class="aws"></div>
            <div class="typescript"></div>
            <div class="laravel"></div>
        </div>
        <p class="section__subtitle subtitle-2">
			Lets work together. <a href="https://www.linkedin.com/in/johndavedecano/" class="connect">Connect with me</a>
		</p>
	</div>
</div>

<style lang="postcss">
    .connect {
        @apply text-yellow-300;
    }
    .logos {
        display: flex;
        flex-wrap: wrap;
        gap: 16px;
        .svelte {
            width: 50px;
            height: 50px;
            background-image: url('svelte.png');
            background-size: 50%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .javascript {
            width: 50px;
            height: 50px;
            background-image: url('js.png');
            background-size: 60%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .node {
            width: 50px;
            height: 50px;
            background-image: url('node.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .react {
            width: 50px;
            height: 50px;
            background-image: url('react.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .vue {
            width: 50px;
            height: 50px;
            background-image: url('vue.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .php {
            width: 50px;
            height: 50px;
            background-image: url('php.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .aws {
            width: 50px;
            height: 50px;
            background-image: url('aws.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .typescript {
            width: 50px;
            height: 50px;
            background-image: url('typescript.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .laravel {
            width: 50px;
            height: 50px;
            background-image: url('laravel.png');
            background-size: 70%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
        .css {
            width: 50px;
            height: 50px;
            background-image: url('css.svg');
            background-size: 90%;
            background-position: center;
            background-repeat: no-repeat;
            background-color: white;
            border-radius: 50%;
        }
    }
	.section-1 {
		@apply bg-blue-950 overflow-hidden;
	}
	.section-1__bg {
		background-image: url('bg-1.jpg');
		width: 100%;
		height: 100%;
		opacity: 0.25;
		background-size: cover;
		position: absolute;
		top: 0;
		right: 0;
		left: 0;
		bottom: 0;
	}
	.section-2 {
		@apply bg-blue-950  overflow-hidden;
	}
	.section-2__bg {
		background-image: url('bg-2.jpg');
		width: 100%;
		height: 100%;
		background-size: cover;
		background-position: bottom left;
		background-repeat: no-repeat;
		position: absolute;
		top: 0;
		right: 0;
		left: 0;
		bottom: 0;
		z-index: 0;
		opacity: 0.25;
	}
	.section-2__person {
		background-image: url('header-small.png');
		width: 100%;
		height: 100%;
		background-size: contain;
		background-position: bottom right;
		background-repeat: no-repeat;
		position: absolute;
		top: 0;
		right: 0;
		left: 0;
		bottom: 0;
		z-index: 1;
		opacity: 0.5;
	}
	.section-2 .section__body {
		@apply text-left flex flex-col gap-4;
        z-index: 2;
	}
	.section {
		@apply w-full flex items-center justify-center relative;
		min-height: 100vh;
	}
	.section__body {
		@apply px-4 w-full lg:w-1/2 text-center;
	}
	.section__title {
		@apply text-white text-6xl lg:text-8xl;
		text-wrap: balance;
	}
	.section__subtitle {
		@apply text-white text-2xl lg:text-4xl;
		text-wrap: balance;
	}
	.section__line {
		width: 100%;
		height: 10px;
		background-color: white;
	}
	.text-accent {
		@apply text-blue-300;
	}
</style>

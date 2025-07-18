<script lang="ts">
    import { onMount } from 'svelte';
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    // Register ScrollTrigger plugin
    gsap.registerPlugin(ScrollTrigger);

    onMount(() => {
        // Animation for h1 (Who We Are) on page load
        gsap.from('.heading', {
            opacity: 0,
            y: 50,
            duration: 1,
            delay: 0.5,
            ease: 'power3.out'
        });

        // Animation for first paragraph and image when they enter viewport
        gsap.from('.initial-content', {
            opacity: 0,
            y: 50,
            duration: 1.2,
            ease: 'power3.out',
            scrollTrigger: {
                trigger: '.initial-content',
                start: 'top 90%', // Adjusted for better mobile visibility
                toggleActions: 'play none none none'
            }
        });

        // Animation for second paragraph when it enters viewport
        gsap.from('.second-paragraph-hero', {
            opacity: 0,
            y: 50,
            duration: 1.2,
            ease: 'power3.out',
            scrollTrigger: {
                trigger: '.second-paragraph-hero',
                start: 'top 90%',
                toggleActions: 'play none none none'
            }
        });
    });
</script>

<div class="mx-4 sm:mx-8 md:mx-16 lg:mx-32 my-6 sm:my-8 md:my-12 min-h-screen">
    <h1 class="mb-6 sm:mb-8 md:mb-10 text-2xl sm:text-3xl md:text-4xl font-extrabold text-base-200 heading">
        Who We Are
    </h1>
    <div
        class="bg-gray-800 bg-opacity-90 text-base-200 rounded-xl px-4 py-4 sm:px-6 sm:py-6 md:px-10 md:py-10 lg:px-16 lg:py-16 shadow-xl backdrop-blur-sm max-w-full"
    >
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 sm:gap-6 md:gap-8 items-center">
            <div>
                <p class="font-bold mb-4 sm:mb-6 text-base sm:text-lg md:text-xl leading-relaxed tracking-wide text-base-300 initial-content">
                    Founded in 2015, LAmpVolt is a trailblazer in blending innovation with everyday life,
                    delivering cutting-edge electronic home appliances and agricultural products. Our journey
                    began with a vision to transform homes and farms by creating solutions that prioritize
                    convenience, productivity, and sustainability, with a product portfolio including Motor
                    Sensor, Home Automation, Battery Cycle, and Smart Extension Board.
                </p>
                <p class="font-semibold text-base sm:text-lg leading-relaxed tracking-wider text-base-500 mb-4 sm:mb-6 second-paragraph-hero">
                    We exceed industry standards with eco-friendly manufacturing, ensuring every product
                    enhances modern living and farming efficiently.
                </p>
            </div>
            <div class="initial-content">
                <img
                    src="/imgs/about-img.webp"
                    alt="who we are"
                    class="w-full h-auto rounded-lg shadow-2xl transform hover:scale-105 transition-transform duration-300"
                />
            </div>
        </div>
    </div>
</div>
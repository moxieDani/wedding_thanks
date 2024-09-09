<script lang="ts">
  import { onMount } from 'svelte';
  import Bowser from 'bowser';
  import Sentence from '@/components/Sentence.svelte';

  let observer: any;

  const setScreenSize = () => {
    const vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
  };

  onMount(() => {
    const parser = Bowser.getParser(window.navigator.userAgent);
    if (parser.getPlatformType() !== 'mobile') {
      window.addEventListener('resize', setScreenSize);
    }
    setScreenSize();

    observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (!entry.isIntersecting) {
            entry.target.classList.remove("fade-in");
          } else {
            entry.target.classList.add("fade-in");
          }
        });
      },
      { threshold: 0.1 }
    );

    const targetElements = document.querySelectorAll(".fade-wrap");
    targetElements.forEach((element) => {
      observer.observe(element);
    });

    return () => {
      observer.disconnect();
    };
  });
</script>

<main>
  <div class="pv-box">
    <div class="fade-wrap">
      <Sentence />
    </div>
  </div>
</main>

<style>
  main {
    position: relative;
    height: calc(var(--vh, 1vh) * 100);
  }
  .seperator {
    background-color: #f8f9fa;
    height: 1rem;
  }
  .pv-box {
    width: 100%;
    height: 100%;
    overflow-y: scroll;
  }
  .pv-box .fade-wrap {
    transition: 2.5s;
    opacity: 1;
  }
  .pv-box .fade-wrap:not(.fade-in) {
    opacity: 0;
  }
</style>

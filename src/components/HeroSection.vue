<script setup lang="ts">
import heroDesktop from "../assets/images/image-hero-desktop.webp";
import heroTablet from "../assets/images/image-hero-tablet.webp";
import heroMobile from "../assets/images/image-hero-mobile.webp";
import UiButton from "./ui/UiButton.vue";
import HeroHeader from "./HeroHeader.vue";
</script>

<template>
  <section>
    <div class="hero-layout container">

      <HeroHeader />

      <div class="hero-content">
        <div class="hero-grid">
          <div class="hero-text">
            <h1 class="text-1">Join the ultimate tech book club</h1>
            <p class="hero-description">
              Turn your reading time into learning time with fellow tech
              enthusiasts. Get curated recommendations, join vibrant
              discussions, and level up your skills one chapter at a time.
            </p>

            <UiButton buttonText="REVIEW MEMBERSHIP OPTIONS" />

            <div class="user-stats">user stats</div>
          </div>
          <picture>
            <source
              :srcset="heroDesktop"
              media="(min-width: 64rem)"
              type="image/webp"
            />
            <source
              :srcset="heroTablet"
              media="(min-width: 40rem)"
              type="image/webp"
            />
            <img
              class="hero-image"
              :src="heroMobile"
              alt="Tech Book Club Hero"
              width="686"
              height="744"
            />
          </picture>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero-layout {
  .hero-header {
    padding-top: var(--spacing-200); // Logo için sadece 16px üstten boşluk
  }

  .hero-image {
    img {
      width: 100%;
      height: auto;
      object-fit: cover;
      border-radius: var(--radius-16);
    }
  }

  .hero-content {
    padding-block: var(--spacing-1000);

    .hero-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: var(--spacing-800);
      align-items: center;

      .hero-text {
        .text-1 {
          margin-top: var(--spacing-400);
          background-image: var(--gradient-text);
          background-clip: text;
          -webkit-background-clip: text;
          color: transparent;
          -webkit-text-fill-color: transparent;
        }

        .hero-description {
          margin: 0; // Varsayılan margin'i sıfırla
          margin-top: var(--spacing-400);
        }
      }
    }
    .hero-image {
      border-radius: var(--radius-10);
    }
  }
}
</style>

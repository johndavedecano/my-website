<div class="wrapper">
  <div class="hero-section">
    <div class="hero-overlay" />
    <div class="hero-content">
      <div class="hero-content-inner">
        <div class="hero-description">
          <div class="hero-title">
            Hello I'm<br /><span>John Dave</span>
          </div>
          <div class="hero-body">
            I am your friendly neighborhood full-stack developer, and I'm
            thrilled to welcome you to my digital domain. With a passion for
            crafting elegant and efficient solutions, I dive into the intricate
            world of web development, equipped with a creative mind and a knack
            for problem-solving.
          </div>
          <a href="mailto:johndavedecano@gmail.com" class="hero-button"
            >Contact Me</a
          >
        </div>
      </div>
    </div>
  </div>
  <div class="connect">
    <div class="connect-title">More About Me</div>
    <p>
      I specialize in building seamless, user-friendly experiences that not only
      captivate the eye but also engage the mind.
    </p>
    <p>
      Whether it's the artistry of front-end design or the robustness of
      back-end functionalities, I thrive on creating interactive and responsive
      web applications that leave a lasting impression.
    </p>
    <p>
      My journey in the realm of technology has been a dynamic one, marked by a
      constant thirst for knowledge and a drive to innovate. Armed with a
      diverse skill set encompassing HTML, CSS, JavaScript, TypeScript, PHP,
      Elixir, and a plethora of frameworks and libraries, I breathe life into
      digital ideas and transform them into functional realities.
    </p>
  </div>
  <div class="connect">
    <div class="connect-items">
      <div class="connect-item">
        <a href="https://www.linkedin.com/in/johndavedecano/">
          <img src="/linkedin.png" alt="" />
        </a>
      </div>
      <div class="connect-item">
        <a href="https://twitter.com/jdecano_js">
          <img src="/twitter.png" alt="" />
        </a>
      </div>
      <div class="connect-item">
        <a href="https://www.facebook.com/profile.php?id=100085142110633">
          <img src="/facebook.png" alt="" />
        </a>
      </div>
      <div class="connect-item">
        <a href="https://github.com/johndavedecano">
          <img src="/github.png" alt="" />
        </a>
      </div>
    </div>
  </div>
</div>

<style lang="postcss">
  .wrapper {
    @apply w-screen h-screen;
  }

  .connect p {
    @apply mb-6;
  }

  .connect {
    @apply px-6 mx-auto;
    width: 1200px;
    max-width: 100%;
  }

  .connect-item {
    @apply flex-1 font-bold text-gray-600 text-center flex items-center justify-center;
    opacity: 0.25;
    transition: all 200ms ease-in-out;
  }

  .connect-item:hover {
    opacity: 1;
  }

  .connect-item img {
    max-width: 120px;
    height: auto;
  }

  .connect-items {
    @apply flex gap-5 flex-col;
  }

  .connect-title {
    @apply text-2xl font-bold text-green-950 mb-6;
  }

  .hero-section {
    @apply flex items-center px-6 py-8 relative mb-12;
    height: 700px;
    background-image: url("/header-small.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }

  .hero-content {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
    z-index: 5;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .hero-title {
    @apply text-6xl font-bold text-white mb-6 lg:text-8xl drop-shadow-lg;
    line-height: 1.5;
  }

  .hero-title > span {
    @apply bg-green-600 px-6;
  }

  .hero-button {
    @apply px-5 py-4 text-white border  bg-green-600 border-green-600 text-2xl font-bold;
    transition: all 200ms ease-in-out;
  }

  .hero-button:hover {
    @apply bg-green-900 border-green-950;
  }

  .hero-body {
    @apply text-base font-semibold text-gray-100 mb-12 lg:text-lg drop-shadow-md;
  }

  .hero-description {
    width: 720px;
    max-width: 100%;
  }

  .hero-content-inner {
    width: 1200px;
    max-width: 100%;
    @apply px-10;
  }

  .hero-overlay {
    @apply bg-green-600;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
    opacity: 0.25;
    z-index: 5;
  }

  @media (min-width: 769px) {
    .hero-section {
      background-image: url("/header.jpg");
    }

    .connect-items {
      @apply flex flex-row;
    }
  }
</style>

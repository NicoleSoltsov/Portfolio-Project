<template>
  <main class="home">
    <section class="hero">
      <div class="left">
        <p class="eyebrow">Brooklyn Raised • Los Angeles Bound</p>

        <h1>Nicole Soltsov</h1>

        <p class="subtitle">
          Computer Science student at UCLA building technology with creativity,
          community, and curiosity.
        </p>

        <div class="tags">
          <span>Developer</span>
          <span>Mentor</span>
          <span>Leader</span>
          <span>Problem Solver</span>
        </div>
      </div>

      <div class="display-box">
        <div class="gold-corner top-left">✦</div>
        <div class="gold-corner top-right">✦</div>

        <p class="box-title">Today's Selection</p>
        <p class="box-subtitle">choose a macaron</p>

        <div class="macaron-grid">
          <RouterLink to="/about" class="macaron pink">
            <span>Rose</span>
            About
          </RouterLink>

          <RouterLink to="/experience" class="macaron blue">
            <span>Blueberry</span>
            Experience
          </RouterLink>

          <RouterLink to="/projects" class="macaron green">
            <span>Pistachio</span>
            Projects
          </RouterLink>

          <a href="mailto:nesoltsov@gmail.com" class="macaron yellow">
            <span>Vanilla</span>
            Contact
          </a>
        </div>
      </div>
    </section>

    <section class="preview">
      <p class="section-label">featured selections</p>
      <h2>A taste of my work</h2>

      <div class="preview-grid">
        <div class="preview-card rose-card">
          <p class="flavor">Community</p>
          <h3>Girls Who Code</h3>   
          <p>Co-founded a coding space focused on confidence, mentorship, and belonging.</p>
        </div>

        <div class="preview-card blue-card">
          <p class="flavor">Backend</p>
          <h3>AI Video Summarizer</h3>
          <p>Built a tool that turns videos into organized summaries, tags, and notes.</p>
        </div>

        <div class="preview-card green-card">
          <p class="flavor">Full Stack</p>
          <h3>K-Drama Tracker</h3>
          <p>Designed a personal tracker for shows, reviews, progress, and reflections.</p>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.home {
  min-height: 100vh;
  padding: 0 8% 90px;
  background:
    radial-gradient(circle at 10% 10%, rgba(244, 214, 220, 0.35), transparent 30%),
    radial-gradient(circle at 90% 90%, rgba(219, 232, 245, 0.45), transparent 32%),
    linear-gradient(180deg, #faf7f2 0%, #fffaf7 100%);
}

.hero {
  min-height: 78vh;
  display: grid;
  grid-template-columns: 1fr 0.9fr;
  align-items: center;
  gap: 70px;
}

.eyebrow {
  color: var(--ucla-blue);
  font-weight: 800;
  letter-spacing: 0.08em;
  margin-bottom: 24px;
  text-transform: uppercase;
  font-size: 0.78rem;
}

h1 {
  font-family: Georgia, serif;
  font-size: clamp(4rem, 8vw, 6.8rem);
  font-weight: 400;
  line-height: 0.95;
  margin-bottom: 24px;
  color: #352b27;
}

.subtitle {
  font-size: 1.25rem;
  line-height: 1.8;
  max-width: 620px;
  color: #5f5651;
}

.tags {
  display: flex;
  gap: 12px;
  margin-top: 32px;
  flex-wrap: wrap;
}

.tags span {
  background: rgba(255, 255, 255, 0.82);
  padding: 12px 20px;
  border-radius: 999px;
  box-shadow: 0 12px 28px rgba(45, 45, 45, 0.07);
  border: 1px solid rgba(178, 131, 65, 0.16);
  font-weight: 700;
}

.display-box {
  position: relative;
  background:
    linear-gradient(145deg, rgba(255, 255, 255, 0.92), rgba(255, 248, 250, 0.9));
  padding: 42px;
  border-radius: 38px;
  box-shadow:
    0 30px 80px rgba(116, 72, 82, 0.14),
    inset 0 0 0 1px rgba(255, 255, 255, 0.75);
  border: 1px solid rgba(178, 131, 65, 0.24);
}

.display-box::before {
  content: "";
  position: absolute;
  inset: 14px;
  border: 1px solid rgba(178, 131, 65, 0.22);
  border-radius: 28px;
  pointer-events: none;
}

.gold-corner {
  position: absolute;
  top: 22px;
  color: #b28341;
  font-size: 1rem;
}

.top-left {
  left: 28px;
}

.top-right {
  right: 28px;
}

.box-title {
  font-family: Georgia, serif;
  font-size: 1.8rem;
  color: #6f4e37;
  text-align: center;
  margin-bottom: 6px;
}

.box-subtitle {
  text-align: center;
  color: #9b735d;
  font-size: 0.78rem;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  margin-bottom: 30px;
}

.macaron-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
}

.macaron {
  min-height: 130px;
  border-radius: 999px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #352b27;
  text-decoration: none;
  font-weight: 800;
  font-size: 1.12rem;
  box-shadow:
    inset 0 -12px rgba(0, 0, 0, 0.06),
    inset 0 9px rgba(255, 255, 255, 0.45),
    0 15px 30px rgba(0, 0, 0, 0.09);
  transition: 0.25s ease;
  position: relative;
}

.macaron::after {
  content: "";
  position: absolute;
  inset: 9px;
  border-radius: 999px;
  border: 1px dashed rgba(255, 255, 255, 0.6);
}

.macaron:hover {
  transform: translateY(-8px) scale(1.03);
}

.macaron span {
  font-family: Georgia, serif;
  font-style: italic;
  font-size: 0.86rem;
  opacity: 0.65;
  margin-bottom: 5px;
}

.pink {
  background: #f4d6dc;
}

.blue {
  background: #dbe8f5;
}

.green {
  background: #dfe9de;
}

.yellow {
  background: #f8e8b8;
}

.preview {
  margin-top: 24px;
}

.section-label {
  color: #9b735d;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  font-size: 0.76rem;
  margin-bottom: 10px;
}

.preview h2 {
  font-family: Georgia, serif;
  font-size: 2.7rem;
  font-weight: 400;
  margin-bottom: 28px;
  color: #352b27;
}

.preview-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.preview-card {
  background: rgba(255, 255, 255, 0.9);
  padding: 30px;
  border-radius: 28px;
  box-shadow: 0 18px 44px rgba(45, 45, 45, 0.07);
  border: 1px solid rgba(178, 131, 65, 0.15);
}

.flavor {
  font-family: Georgia, serif;
  font-style: italic;
  margin-bottom: 10px;
  color: #9b735d;
}

.preview-card h3 {
  margin-bottom: 10px;
  font-size: 1.3rem;
}

.preview-card p {
  line-height: 1.65;
  color: #5f5651;
}

@media (max-width: 900px) {
  .hero,
  .preview-grid {
    grid-template-columns: 1fr;
  }

  .hero {
    padding-top: 40px;
  }

  .macaron-grid {
    grid-template-columns: 1fr;
  }
}
</style>
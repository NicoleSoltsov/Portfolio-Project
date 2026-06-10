<template>
  <main class="about">
    <section class="about-hero">
      <div class="portrait-card">
        <div class="photo-frame">
          <img src="/nicole.jpg" alt="Nicole Soltsov" class="profile-photo" />
        </div>

        <div class="caption-card">
          <p class="caption-name">Nicole Soltsov</p>
          <p>UCLA Computer Science</p>
        </div>
      </div>

      <div class="story-card">
        <p class="eyebrow">About Me</p>
        <h1>Building with care, curiosity, and community.</h1>

        <p>
          Hi, I’m Nicole — a Computer Science student at UCLA from Brooklyn, New York.
          I love building projects that connect my technical side with the parts of me that
          are creative, detail-oriented, and community-driven.
        </p>

        <p>
          I first got into computer science by teaching myself Python and realizing that
          coding could turn an idea into something real. Since then, I’ve built full-stack
          projects, explored AI tools, and co-founded Girls Who Code at my high school to
          help other students feel less intimidated when they are just starting out.
        </p>

        <div class="mini-macarons">
          <span>AI</span>
          <span>Full Stack</span>
          <span>Education Tech</span>
          <span>Creative Tools</span>
        </div>
      </div>
    </section>

    <section class="recipe-section">
      <div class="recipe-card">
        <p class="section-label">A little more about me</p>
        <h2>My recipe</h2>

        <div class="recipe-grid">
          <div class="recipe-item">
            <span>01</span>
            <h3>Community-first</h3>
            <p>
              I like making technical spaces feel more welcoming, especially for beginners.
            </p>
          </div>

          <div class="recipe-item">
            <span>02</span>
            <h3>Creative builder</h3>
            <p>
              My favorite projects mix code with personality, design, and storytelling.
            </p>
          </div>

          <div class="recipe-item">
            <span>03</span>
            <h3>Detail-oriented</h3>
            <p>
              I care about the small choices that make a product feel polished and easy to use.
            </p>
          </div>

          <div class="recipe-item">
            <span>04</span>
            <h3>Always learning</h3>
            <p>
              I’m drawn to problems that make me think harder, ask better questions, and keep improving.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section class="values">
      <p class="section-label">My Ingredients</p>
      <h2>What I bring to the table</h2>

      <div class="values-grid">
        <div class="value-card rose-card">
          <p class="flavor">Rose</p>
          <h3>Community</h3>
          <p>
            Through Girls Who Code, tutoring, and mentoring younger students, I’ve learned that
            tech feels less intimidating when people have someone beside them saying, “You belong here.”
          </p>
        </div>

        <div class="value-card blueberry-card">
          <p class="flavor">Blueberry</p>
          <h3>Curiosity</h3>
          <p>
            I like understanding how things work behind the scenes — from backend pipelines
            and APIs to the small design choices that make a product easier to use.
          </p>
        </div>

        <div class="value-card pistachio-card">
          <p class="flavor">Pistachio</p>
          <h3>Creativity</h3>
          <p>
            My favorite projects combine technical problem-solving with personality, whether
            that means building a K-drama tracker, a classroom app, or a tool that makes
            information easier to understand.
          </p>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.about {
  min-height: 100vh;
  padding: 60px 8% 90px;
  background:
    radial-gradient(circle at 10% 15%, rgba(244, 214, 220, 0.35), transparent 32%),
    radial-gradient(circle at 90% 85%, rgba(219, 232, 245, 0.35), transparent 32%),
    linear-gradient(180deg, #faf7f2 0%, #fffaf7 100%);
}

.about-hero {
  display: grid;
  grid-template-columns: 0.85fr 1.15fr;
  gap: 60px;
  align-items: stretch;
}

.portrait-card,
.story-card,
.recipe-card,
.value-card {
  background: rgba(255, 255, 255, 0.92);
  border: 1px solid rgba(178, 131, 65, 0.18);
  box-shadow: 0 18px 44px rgba(45, 45, 45, 0.07);
}

.portrait-card {
  border-radius: 38px;
  padding: 34px;
  position: relative;
  overflow: hidden;
}

.portrait-card::before,
.story-card::before,
.recipe-card::before {
  content: "";
  position: absolute;
  inset: 14px;
  border: 1px solid rgba(178, 131, 65, 0.18);
  border-radius: 28px;
  pointer-events: none;
}

.photo-frame {
  display: flex;
  justify-content: center;
}

.profile-photo {
  width: 100%;
  max-width: 330px;
  height: 430px;
  object-fit: cover;
  object-position: center;
  border-radius: 30px;
  border: 8px solid white;
  box-shadow:
    0 18px 40px rgba(0, 0, 0, 0.12),
    0 0 0 1px rgba(178, 131, 65, 0.18);
}

.caption-card {
  margin: 24px auto 0;
  max-width: 330px;
  background: #fff8fa;
  border: 1px solid rgba(178, 131, 65, 0.18);
  border-radius: 22px;
  padding: 18px;
  text-align: center;
}

.caption-name {
  font-family: Georgia, serif;
  font-size: 1.4rem;
  color: #352b27;
}

.caption-card p:last-child {
  color: #9b735d;
  margin-top: 4px;
}

.story-card {
  border-radius: 38px;
  padding: 50px;
  position: relative;
  overflow: hidden;
}

.story-card::after {
  content: "✦";
  position: absolute;
  right: 34px;
  top: 28px;
  color: rgba(178, 131, 65, 0.6);
  font-size: 1.4rem;
}

.eyebrow,
.section-label {
  color: var(--ucla-blue);
  font-weight: 800;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  font-size: 0.78rem;
  margin-bottom: 18px;
}

h1,
h2 {
  font-family: Georgia, serif;
  color: #352b27;
  font-weight: 400;
}

h1 {
  font-size: clamp(2.8rem, 5vw, 4.7rem);
  line-height: 1;
  margin-bottom: 28px;
}

.story-card p {
  color: #5f5651;
  font-size: 1.08rem;
  line-height: 1.85;
  margin-bottom: 18px;
}

.mini-macarons {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 28px;
}

.mini-macarons span {
  padding: 11px 18px;
  border-radius: 999px;
  font-weight: 700;
  color: #4f4641;
  box-shadow:
    inset 0 -6px rgba(0, 0, 0, 0.04),
    0 10px 20px rgba(45, 45, 45, 0.06);
}

.mini-macarons span:nth-child(1) {
  background: #f4d6dc;
}

.mini-macarons span:nth-child(2) {
  background: #dbe8f5;
}

.mini-macarons span:nth-child(3) {
  background: #dfe9de;
}

.mini-macarons span:nth-child(4) {
  background: #f8e8b8;
}

.recipe-section {
  margin-top: 70px;
}

.recipe-card {
  border-radius: 38px;
  padding: 46px;
  position: relative;
}

.recipe-card h2 {
  font-size: 2.7rem;
  margin-bottom: 30px;
}

.recipe-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 18px;
}

.recipe-item {
  background: #fffaf7;
  border: 1px solid rgba(178, 131, 65, 0.14);
  border-radius: 24px;
  padding: 24px;
}

.recipe-item span {
  display: inline-flex;
  width: 38px;
  height: 38px;
  border-radius: 50%;
  align-items: center;
  justify-content: center;
  background: #f4d6dc;
  color: #6f4e37;
  font-weight: 800;
  margin-bottom: 18px;
}

.recipe-item h3,
.value-card h3 {
  color: #352b27;
  font-size: 1.25rem;
  margin-bottom: 10px;
}

.recipe-item p,
.value-card p {
  color: #5f5651;
  line-height: 1.65;
}

.values {
  margin-top: 80px;
}

.values h2 {
  font-size: 2.7rem;
  margin-bottom: 28px;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.value-card {
  padding: 30px;
  border-radius: 28px;
  position: relative;
  overflow: hidden;
}

.value-card::before {
  content: "";
  position: absolute;
  width: 90px;
  height: 45px;
  border-radius: 999px;
  right: -18px;
  top: 20px;
  opacity: 0.6;
}

.rose-card::before {
  background: #f4d6dc;
}

.blueberry-card::before {
  background: #dbe8f5;
}

.pistachio-card::before {
  background: #dfe9de;
}

.flavor {
  font-family: Georgia, serif;
  font-style: italic;
  color: #9b735d;
  margin-bottom: 10px;
}

@media (max-width: 1000px) {
  .about-hero,
  .recipe-grid,
  .values-grid {
    grid-template-columns: 1fr;
  }

  .story-card,
  .portrait-card,
  .recipe-card {
    padding: 34px;
  }

  .profile-photo {
    height: 360px;
  }
}
</style>
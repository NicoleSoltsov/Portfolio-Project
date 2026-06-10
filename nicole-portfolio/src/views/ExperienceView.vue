<template>
  <main class="experience">
    <section class="hero">
      <p class="eyebrow">Experience</p>
      <h1>The experiences that shaped me.</h1>
      <p class="subtitle">
        A collection of coding, leadership, teaching, athletics, and creativity — each one
        shaping how I build, lead, and learn.
      </p>
    </section>

    <section class="experience-box">
      <article class="story-card rose-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2023 — Present</p>
          <h2>Girls Who Code</h2>
          <p class="role">Co-Founder & Co-President</p>
          <p>
            What started as a small idea became one of the most meaningful parts of my high
            school experience. I created beginner lessons in Python and Java, organized guest
            speakers, and helped students discover that computer science was something they
            belonged in.
          </p>
        </div>
      </article>

      <article class="story-card blueberry-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2024 — 2025</p>
          <h2>Building Software</h2>
          <p class="role">Summer Design Institute Computer Science Intern</p>
          <p>
            My favorite internship project was building a K-Drama tracker using Django and Vue.
            Users could track shows, ratings, reviews, and OSTs through TMDB and Spotify
            integrations. I also used Python to support an energy-saving plan for the school year.
          </p>
        </div>
      </article>

      <article class="story-card pistachio-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2022 — Present</p>
          <h2>Tennis</h2>
          <p class="role">Captain, Second Singles, Volunteer Coach</p>
          <p>
            Tennis taught me leadership long before I became captain. As a four-year varsity
            player, NYS Scholar Athlete, PSAL team finalist, and volunteer coach, I learned how
            to support teammates, stay resilient under pressure, and lead by example.
          </p>
        </div>
      </article>

      <article class="story-card vanilla-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2024 — 2025</p>
          <h2>Teaching & Mentoring</h2>
          <p class="role">Math Tutor, Tennis Coach, English Teacher Assistant</p>
          <p>
            Whether I’m tutoring algebra, coaching tennis, or helping grade freshman English
            assignments, I enjoy helping others learn. Teaching has strengthened the way I explain
            ideas and reminded me how much confidence can grow with the right support.
          </p>
        </div>
      </article>

      <article class="story-card lavender-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2023 — 2025</p>
          <h2>Creativity Beyond Computer Science</h2>
          <p class="role">Electric Guitar & Creative Writing in London</p>
          <p>
            Outside of STEM, I like creative challenges that make me think differently. I taught
            myself electric guitar through independent practice, and I studied creative writing
            abroad in London while exploring literature, storytelling, and culture.
          </p>
        </div>
      </article>

      <article class="story-card butter-card">
        <div class="image-placeholder">Image</div>

        <div class="content">
          <p class="date">2023 — 2025</p>
          <h2>Always Learning</h2>
          <p class="role">College Now & Girls Who Code Summer Immersion</p>
          <p>
            Through College Now courses in web development and computer game programming, along
            with the Girls Who Code Summer Immersion Program, I explored JavaScript, game
            development, collaboration, and the skills that led me further into computer science.
          </p>
        </div>
      </article>
    </section>

    <section class="skills-section">
      <p class="section-label">Technical Shelf</p>
      <h2>Skills I’ve been building</h2>

      <div class="skills">
        <span>Python</span>
        <span>JavaScript</span>
        <span>HTML/CSS</span>
        <span>Vue</span>
        <span>Django</span>
        <span>Express</span>
        <span>AutoCAD</span>
        <span>Inventor</span>
        <span>Russian</span>
      </div>
    </section>
  </main>
</template>

<style scoped>
.experience {
  min-height: 100vh;
  padding: 60px 8% 90px;
  background:
    radial-gradient(circle at 12% 12%, rgba(244, 214, 220, 0.34), transparent 32%),
    radial-gradient(circle at 88% 88%, rgba(219, 232, 245, 0.38), transparent 32%),
    linear-gradient(180deg, #faf7f2 0%, #fffaf7 100%);
}

.hero {
  max-width: 900px;
  margin-bottom: 54px;
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
  font-size: clamp(3.2rem, 7vw, 6rem);
  line-height: 0.98;
  margin-bottom: 22px;
}

.subtitle {
  color: #5f5651;
  font-size: 1.18rem;
  line-height: 1.75;
  max-width: 760px;
}

.experience-box {
  display: grid;
  gap: 26px;
}

.story-card {
  position: relative;
  display: grid;
  grid-template-columns: 260px 1fr;
  gap: 30px;
  align-items: center;
  background: rgba(255, 255, 255, 0.92);
  border: 1px solid rgba(178, 131, 65, 0.16);
  box-shadow: 0 18px 44px rgba(45, 45, 45, 0.07);
  border-radius: 34px;
  padding: 34px;
  overflow: hidden;
}

.story-card::before {
  content: "";
  position: absolute;
  inset: 14px;
  border: 1px solid rgba(178, 131, 65, 0.14);
  border-radius: 24px;
  pointer-events: none;
}

.image-placeholder {
  width: 100%;
  height: 185px;
  border-radius: 26px;
  border: 2px dashed rgba(178, 131, 65, 0.32);
  background:
    linear-gradient(145deg, rgba(244, 214, 220, 0.34), rgba(255, 255, 255, 0.85)),
    radial-gradient(circle at top right, rgba(219, 232, 245, 0.55), transparent 60%);
  display: flex;
  align-items: center;
  justify-content: center;
  color: #9b735d;
  font-family: Georgia, serif;
  font-style: italic;
  box-shadow:
    inset 0 0 0 8px rgba(255, 255, 255, 0.45),
    0 12px 30px rgba(45, 45, 45, 0.06);
  z-index: 1;
}

.content {
  z-index: 1;
}

.date {
  font-family: Georgia, serif;
  font-style: italic;
  color: #9b735d;
  margin-bottom: 8px;
}

.story-card h2 {
  font-size: 2rem;
  margin-bottom: 8px;
}

.role {
  color: var(--ucla-blue);
  font-weight: 800;
  margin-bottom: 14px;
}

.story-card p {
  color: #5f5651;
  line-height: 1.7;
}

.skills-section {
  margin-top: 76px;
  background: rgba(255, 255, 255, 0.9);
  border: 1px solid rgba(178, 131, 65, 0.16);
  box-shadow: 0 18px 44px rgba(45, 45, 45, 0.07);
  border-radius: 34px;
  padding: 38px;
}

.skills-section h2 {
  font-size: 2.5rem;
  margin-bottom: 26px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

.skills span {
  background: #fffaf7;
  border: 1px solid rgba(178, 131, 65, 0.14);
  border-radius: 999px;
  padding: 12px 18px;
  color: #4f4641;
  font-weight: 700;
  box-shadow: 0 10px 22px rgba(45, 45, 45, 0.05);
}

@media (max-width: 820px) {
  .story-card {
    grid-template-columns: 1fr;
  }

  h1 {
    font-size: 3rem;
  }
}
</style>
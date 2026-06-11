<template>
  <main class="projects">
    <section class="hero">
      <p class="eyebrow">Projects</p>
      <h1>Things I’ve built and taught.</h1>
      <p class="subtitle">
        A collection of apps, tools, and curriculum projects that combine software,
        creativity, and community.
      </p>
    </section>

    <section class="project-list">
      <article class="project-card rose-card featured-project">
        <div class="video-card">
          <p class="video-label">Demo</p>
          <h3>K-Drama Tracker Walkthrough</h3>
          <a
            href="https://www.youtube.com/watch?v=pteV4YhKMiU&t=1s"
            target="_blank"
            rel="noopener noreferrer"
            class="video-button"
          >
            Watch Demo
          </a>
        </div>

        <div class="project-content">
          <p class="flavor">Rose</p>
          <h2>K-Drama Tracker App</h2>
          <p class="type">Full-Stack Web App · Django · Vue · TMDB API · Spotify API</p>

          <p>
            A personalized K-drama tracking platform where users can save shows, track
            progress, write reviews, rate dramas, and connect each show to its OSTs through
            Spotify links.
          </p>

          <div class="tags">
            <span>Django</span>
            <span>Vue</span>
            <span>TMDB API</span>
            <span>Spotify API</span>
            <span>Full Stack</span>
          </div>

          <div class="project-links">
            <a
              href="https://www.youtube.com/watch?v=pteV4YhKMiU&t=1s"
              target="_blank"
              rel="noopener noreferrer"
            >
              Website Demo
            </a>

            <a
              href="https://github.com/your-username/kdrama-tracker"
              target="_blank"
              rel="noopener noreferrer"
            >
              GitHub
            </a>
          </div>
        </div>
      </article>

      <article class="project-card blue-card">
        <div class="project-icon backend-icon">
          <span>AI</span>
        </div>

        <div class="project-content">
          <p class="flavor">Blueberry</p>
          <h2>AI Video Summarizer</h2>
          <p class="type">Backend Project · Node · Express · MongoDB · Whisper · GPT</p>

          <p>
            A backend pipeline that processes videos by downloading content, converting audio,
            generating transcripts, and producing organized AI summaries with tags and notes.
          </p>

          <div class="tags">
            <span>Node</span>
            <span>Express</span>
            <span>MongoDB</span>
            <span>Whisper</span>
            <span>GPT</span>
          </div>

          <div class="project-links">
            <a
              href="https://github.com/your-username/ai-video-summarizer"
              target="_blank"
              rel="noopener noreferrer"
            >
              GitHub
            </a>
          </div>
        </div>
      </article>

      <article class="project-card green-card">
        <div class="project-icon polling-icon">
          <span>Poll</span>
        </div>

        <div class="project-content">
          <p class="flavor">Pistachio</p>
          <h2>Classroom Polling App</h2>
          <p class="type">Team Full-Stack App · Django REST Framework · SimpleJWT</p>

          <p>
            A Mentimeter-style classroom platform with join codes, live polls, quizzes,
            participant responses, and a planned leaderboard/live update system for teachers.
          </p>

          <div class="tags">
            <span>Django REST</span>
            <span>JWT Auth</span>
            <span>Polls</span>
            <span>Quizzes</span>
            <span>Team Project</span>
          </div>

          <div class="project-links">
            <a
              href="https://github.com/your-username/classroom-polling-app"
              target="_blank"
              rel="noopener noreferrer"
            >
              GitHub
            </a>
          </div>
        </div>
      </article>

      <article class="project-card yellow-card">
        <div class="project-icon curriculum-icon">
          <span>Py</span>
        </div>

        <div class="project-content">
          <p class="flavor">Vanilla</p>
          <h2>Girls Who Code Python Curriculum</h2>
          <p class="type">Teaching Project · Python · Beginner Programming</p>

          <p>
            A beginner-friendly curriculum I created for Girls Who Code to introduce students
            to Python through clear lessons, practice problems, and confidence-building
            activities.
          </p>

          <div class="tags">
            <span>Python</span>
            <span>Teaching</span>
            <span>Curriculum</span>
            <span>Mentorship</span>
          </div>

          <div class="project-links">
            <a
              href="https://github.com/your-username/python-curriculum"
              target="_blank"
              rel="noopener noreferrer"
            >
              GitHub
            </a>
          </div>
        </div>
      </article>
    </section>
  </main>
</template>

<style scoped>
.projects {
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

.eyebrow {
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

.project-list {
  display: grid;
  gap: 28px;
}

.project-card {
  position: relative;
  display: grid;
  grid-template-columns: 330px 1fr;
  gap: 34px;
  align-items: center;
  background: rgba(255, 255, 255, 0.92);
  border: 1px solid rgba(178, 131, 65, 0.16);
  box-shadow: 0 18px 44px rgba(45, 45, 45, 0.07);
  border-radius: 36px;
  padding: 34px;
  overflow: hidden;
}

.project-card::before {
  content: "";
  position: absolute;
  inset: 14px;
  border: 1px solid rgba(178, 131, 65, 0.14);
  border-radius: 26px;
  pointer-events: none;
}

.project-card::after {
  content: "";
  position: absolute;
  width: 145px;
  height: 72px;
  border-radius: 999px;
  right: -32px;
  top: 28px;
  opacity: 0.5;
}

.rose-card::after {
  background: #f4d6dc;
}

.blue-card::after {
  background: #dbe8f5;
}

.green-card::after {
  background: #dfe9de;
}

.yellow-card::after {
  background: #f8e8b8;
}

.video-card,
.project-icon {
  height: 215px;
  border-radius: 28px;
  border: 1px solid rgba(178, 131, 65, 0.22);
  background:
    linear-gradient(145deg, rgba(244, 214, 220, 0.42), rgba(255, 255, 255, 0.9)),
    radial-gradient(circle at top right, rgba(219, 232, 245, 0.55), transparent 60%);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow:
    inset 0 0 0 8px rgba(255, 255, 255, 0.45),
    0 12px 30px rgba(45, 45, 45, 0.06);
  z-index: 1;
}

.video-card {
  flex-direction: column;
  text-align: center;
  padding: 24px;
}

.video-label {
  color: var(--ucla-blue);
  font-weight: 800;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  font-size: 0.72rem;
  margin-bottom: 10px;
}

.video-card h3 {
  font-family: Georgia, serif;
  font-size: 1.5rem;
  color: #352b27;
  margin-bottom: 18px;
}

.video-button {
  background: white;
  color: #352b27;
  text-decoration: none;
  border: 1px solid rgba(178, 131, 65, 0.2);
  border-radius: 999px;
  padding: 10px 18px;
  font-weight: 800;
  transition: 0.2s ease;
}

.video-button:hover {
  transform: translateY(-2px);
  background: #fffaf7;
}

.project-icon {
  font-family: Georgia, serif;
  font-size: 2.4rem;
  color: #6f4e37;
  font-weight: 700;
}

.project-icon span {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  box-shadow:
    inset 0 -10px rgba(0, 0, 0, 0.06),
    inset 0 8px rgba(255, 255, 255, 0.45),
    0 14px 30px rgba(0, 0, 0, 0.08);
}

.backend-icon span {
  background: #dbe8f5;
}

.polling-icon span {
  background: #dfe9de;
}

.curriculum-icon span {
  background: #f8e8b8;
}

.project-content {
  z-index: 1;
}

.flavor {
  font-family: Georgia, serif;
  font-style: italic;
  color: #9b735d;
  margin-bottom: 8px;
}

.project-content h2 {
  font-size: 2.2rem;
  margin-bottom: 8px;
}

.type {
  color: var(--ucla-blue);
  font-weight: 800;
  margin-bottom: 16px;
}

.project-content p {
  color: #5f5651;
  line-height: 1.7;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 22px;
}

.tags span {
  background: #fffaf7;
  border: 1px solid rgba(178, 131, 65, 0.14);
  border-radius: 999px;
  padding: 9px 14px;
  color: #4f4641;
  font-weight: 700;
  font-size: 0.9rem;
}

.project-links {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}

.project-links a {
  text-decoration: none;
  background: white;
  color: #352b27;
  border: 1px solid rgba(178, 131, 65, 0.2);
  border-radius: 999px;
  padding: 10px 18px;
  font-weight: 800;
  transition: 0.2s ease;
}

.project-links a:hover {
  transform: translateY(-2px);
  background: #f4d6dc;
}

@media (max-width: 900px) {
  .project-card {
    grid-template-columns: 1fr;
  }

  h1 {
    font-size: 3rem;
  }

  .video-card,
  .project-icon {
    height: 200px;
  }
}
</style>
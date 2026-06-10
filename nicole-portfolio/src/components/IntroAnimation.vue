<script setup>
let hasOpened = false

const emit = defineEmits(['finished'])

function openPortfolio() {
  if (hasOpened) return
  hasOpened = true

  const box = document.querySelector('.macaron-box')
  box.classList.add('opened')

  setTimeout(() => {
    emit('finished')
  }, 3300)
}
</script>

<template>
  <section class="intro">
    <div class="sparkle sparkle-one">✦</div>
    <div class="sparkle sparkle-two">✧</div>
    <div class="sparkle sparkle-three">✦</div>

    <button class="macaron-box" @click="openPortfolio">
      <div class="box-shadow"></div>

      <div class="lid">
        <div class="gold-frame"></div>

        <p class="small-text">THE PORTFOLIO OF</p>
        <h1>Nicole Soltsov</h1>
        <p class="click-text">click to open</p>
      </div>

      <div class="base">
        <div class="tray-line"></div>

        <div class="cup">
          <img src="/macarons/rose.png" alt="Rose macaron" class="macaron-img rose-img" />
          <span class="macaron-label">About</span>
        </div>

        <div class="cup">
          <img src="/macarons/blueberry.png" alt="Blueberry macaron" class="macaron-img blueberry-img" />
          <span class="macaron-label">Experience</span>
        </div>

        <div class="cup">
          <img src="/macarons/pistachio.png" alt="Pistachio macaron" class="macaron-img pistachio-img" />
          <span class="macaron-label">Projects</span>
        </div>

        <div class="cup">
          <img src="/macarons/vanilla.png" alt="Vanilla macaron" class="macaron-img vanilla-img" />
          <span class="macaron-label">Contact</span>
        </div>
      </div>
    </button>
  </section>
</template>

<style scoped>
.intro {
  position: fixed;
  inset: 0;
  background:
    radial-gradient(circle at top left, rgba(244, 214, 220, 0.6), transparent 35%),
    radial-gradient(circle at bottom right, rgba(219, 232, 245, 0.75), transparent 35%),
    #faf7f2;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.macaron-box {
  position: relative;
  width: min(850px, 90vw);
  height: 390px;
  border: none;
  background: transparent;
  cursor: pointer;
  perspective: 1600px;
}

.box-shadow {
  position: absolute;
  bottom: -35px;
  left: 8%;
  width: 84%;
  height: 50px;
  background: rgba(105, 75, 65, 0.18);
  filter: blur(22px);
  border-radius: 50%;
}

.lid {
  position: absolute;
  inset: 0;
  z-index: 5;
  background:
    linear-gradient(145deg, rgba(255, 255, 255, 0.5), transparent 35%),
    linear-gradient(145deg, #f6cbd5, #f9e3e8);
  border-radius: 34px;
  box-shadow:
    0 35px 90px rgba(116, 72, 82, 0.25),
    inset 0 0 0 2px rgba(255, 255, 255, 0.55);
  transform-origin: center bottom;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #6f4e37;
  transition: transform 0.4s ease;
}

.macaron-box:hover .lid {
  transform: translateY(-8px);
}

.macaron-box.opened .lid {
  animation: openLid 2.4s ease forwards;
}

.gold-frame {
  position: absolute;
  inset: 28px;
  border: 2px solid rgba(178, 131, 65, 0.65);
  border-radius: 25px;
}

.gold-frame::before,
.gold-frame::after {
  content: "✦";
  position: absolute;
  top: -15px;
  color: rgba(178, 131, 65, 0.85);
  font-size: 1.2rem;
}

.gold-frame::before {
  left: 30px;
}

.gold-frame::after {
  right: 30px;
}

.small-text {
  font-size: 0.8rem;
  letter-spacing: 0.45em;
  margin-bottom: 16px;
}

.lid h1 {
  font-family: Georgia, serif;
  font-size: clamp(3rem, 7vw, 5.8rem);
  font-weight: 400;
  letter-spacing: 0.02em;
  margin-bottom: 30px;
}

.click-text {
  font-family: Georgia, serif;
  font-style: italic;
  font-size: 1.1rem;
  opacity: 0.8;
}

.base {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 270px;
  background:
    linear-gradient(145deg, rgba(255, 255, 255, 0.65), transparent 30%),
    linear-gradient(145deg, #f2c3cf, #f9dfe6);
  border: 12px solid #f6d8df;
  border-radius: 32px;
  box-shadow:
    0 35px 80px rgba(116, 72, 82, 0.22),
    inset 0 -14px 20px rgba(116, 72, 82, 0.08),
    inset 0 10px 18px rgba(255, 255, 255, 0.65);
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 38px;
  overflow: hidden;
}

.tray-line {
  position: absolute;
  inset: 22px;
  border: 2px solid rgba(255, 255, 255, 0.65);
  border-radius: 24px;
  pointer-events: none;
}

.tray-line::before,
.tray-line::after {
  content: "";
  position: absolute;
  top: 12px;
  bottom: 12px;
  width: 2px;
  background: rgba(255, 255, 255, 0.5);
}

.tray-line::before {
  left: 33%;
}

.tray-line::after {
  right: 33%;
}

.cup {
  position: relative;
  width: 155px;
  height: 155px;
  border-radius: 50%;
  background:
    repeating-conic-gradient(
      from 0deg,
      #fff8f9 0deg 8deg,
      #f1e1e4 8deg 13deg
    );
  display: grid;
  place-items: center;
  box-shadow:
    inset 0 -10px 18px rgba(107, 77, 68, 0.1),
    0 10px 22px rgba(107, 77, 68, 0.12);
  opacity: 0;
  transform: translateY(35px) scale(0.85);
}

.cup::after {
  content: "";
  position: absolute;
  inset: 17px;
  border-radius: 50%;
  background: radial-gradient(circle, #fff 0 44%, #f7eef0 45% 100%);
  box-shadow: inset 0 -8px 12px rgba(107, 77, 68, 0.08);
}

.macaron-img {
  position: relative;
  z-index: 2;
  height: auto;
  object-fit: contain;
  object-position: center;
  filter: drop-shadow(0 14px 16px rgba(75, 47, 42, 0.22));
}

.rose-img {
  width: 140px;
}

.blueberry-img {
  width: 155px;
}

.pistachio-img {
  width: 260px;
  transform: translateY(-60px);
  left: -55px;
}

.vanilla-img {
  width: 200px;
  transform: translateY(-26px);
  left: -25px;
}

.macaron-label {
  position: absolute;
  z-index: 3;
  font-family: Georgia, serif;
  font-weight: 700;
  color: #4a352b;
  background: rgba(255, 255, 255, 0.55);
  padding: 5px 12px;
  border-radius: 999px;
  backdrop-filter: blur(4px);
}

.macaron-box.opened .cup {
  animation: cupPop 0.65s ease forwards;
}

.cup:nth-of-type(2) {
  animation-delay: 0.85s;
}

.cup:nth-of-type(3) {
  animation-delay: 1.05s;
}

.cup:nth-of-type(4) {
  animation-delay: 1.25s;
}

.cup:nth-of-type(5) {
  animation-delay: 1.45s;
}

.sparkle {
  position: absolute;
  color: rgba(178, 131, 65, 0.7);
  font-size: 2rem;
  animation: sparkleFloat 3s ease-in-out infinite;
}

.sparkle-one {
  top: 18%;
  left: 18%;
}

.sparkle-two {
  top: 23%;
  right: 18%;
  animation-delay: 0.8s;
}

.sparkle-three {
  bottom: 18%;
  left: 24%;
  animation-delay: 1.4s;
}

.macaron-box.opened {
  animation: fadeAway 0.9s ease forwards;
  animation-delay: 2.55s;
}

@keyframes openLid {
  0% {
    transform: translateY(0) rotateX(0deg) scale(1);
    opacity: 1;
  }

  40% {
    transform: translateY(-80px) rotateX(12deg) scale(1.01);
    opacity: 1;
  }

  75% {
    transform: translateY(-210px) rotateX(18deg) scale(1.02);
    opacity: 0.95;
  }

  100% {
    transform: translateY(-290px) rotateX(22deg) scale(1.03);
    opacity: 0.85;
  }
}

@keyframes cupPop {
  0% {
    opacity: 0;
    transform: translateY(35px) scale(0.85);
  }

  70% {
    opacity: 1;
    transform: translateY(-14px) scale(1.06);
  }

  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes sparkleFloat {
  0%, 100% {
    transform: translateY(0) rotate(0deg);
    opacity: 0.35;
  }

  50% {
    transform: translateY(-12px) rotate(12deg);
    opacity: 1;
  }
}

@keyframes fadeAway {
  to {
    opacity: 0;
    transform: scale(1.04);
  }
}

@media (max-width: 760px) {
  .macaron-box {
    height: 620px;
  }

  .lid {
    height: 310px;
  }

  .base {
    height: 480px;
    flex-wrap: wrap;
    gap: 18px;
  }

  .cup {
    width: 135px;
    height: 135px;
  }

  .rose-img,
  .blueberry-img {
    width: 125px;
  }

  .pistachio-img {
    width: 155px;
  }

  .vanilla-img {
    width: 150px;
  }

  .macaron-label {
    font-size: 0.85rem;
  }
}
</style>
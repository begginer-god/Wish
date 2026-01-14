

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Happy Birthday | For a Special Soul</title>

    <link
      href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@300;400;600&family=Dancing+Script:wght@700&display=swap"
      rel="stylesheet"
    />

    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      :root {
        --dark-bg: #0a0a0c;
        --navy-bg: #0d1b2a;
        --mint: #00f5ff;
        --pink: #ff70a6;
        --gold: #ddc133;
        --white: #f8f9fa;
      }

      body {
        font-family: Montserrat, sans-serif;
        background: var(--dark-bg);
        color: var(--white);
        min-height: 100vh;
        overflow-x: hidden;
      }

      /* BACKGROUND */
      .aurora-bg {
        position: fixed;
        inset: 0;
        z-index: -2;
        background: radial-gradient(
            circle at top right,
            rgba(221, 21, 98, 0.15),
            transparent 50%
          ),
          radial-gradient(
            circle at bottom left,
            rgba(144, 156, 29, 0.15),
            transparent 50%
          ),
          linear-gradient(135deg, var(--navy-bg), var(--dark-bg));
        filter: blur(60px);
      }

      /* LANDING */
      .landing {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        transition: opacity 1s;
      }

      .landing h1 {
        font-family: "Playfair Display", serif;
        font-size: clamp(2.5rem, 8vw, 5rem);
        background: linear-gradient(135deg, var(--white), var(--gold));
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
      }

      .subtitle {
        font-family: "Dancing Script", cursive;
        font-size: 2.5rem;
        color: var(--pink);
        margin: 1rem 0 2rem;
      }

      .date {
        padding: 0.8rem 2rem;
        border-radius: 50px;
        border: 1px solid rgba(255, 214, 10, 0.4);
        margin-bottom: 3rem;
        color: var(--mint);
      }

      .btn {
        padding: 1.2rem 3.5rem;
        border: none;
        border-radius: 50px;
        font-weight: 600;
        cursor: pointer;
        background: linear-gradient(135deg, var(--pink), var(--gold));
      }

      /* MAIN */
      .main {
        display: none;
        opacity: 0;
        padding: 4rem 1.5rem;
        transition: opacity 1s;
      }

      .container {
        max-width: 1100px;
        margin: auto;
      }

      .title {
        font-family: "Playfair Display", serif;
        font-size: 3rem;
        text-align: center;
        color: var(--gold);
        margin-bottom: 4rem;
      }

      /* CARDS */
      .cards {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 2rem;
      }

      .card {
        background: rgba(255, 255, 255, 0.05);
        border-radius: 25px;
        padding: 2.5rem;
        text-align: center;
        transition: 0.3s;
      }

      .card:hover {
        transform: translateY(-10px);
        border: 1px solid var(--pink);
      }

      .icon {
        font-size: 3rem;
      }

      .card h3 {
        margin: 1rem 0;
        font-family: "Playfair Display", serif;
        color: var(--gold);
      }

      /* WISH */
      .wish {
        margin: 4rem 0;
        padding: 4rem 2rem;
        text-align: center;
        border-radius: 40px;
        background: rgba(0, 245, 255, 0.05);
      }

      .wish p {
        font-family: "Dancing Script", cursive;
        font-size: 2.5rem;
      }

      /* REVEAL */
      .reveal {
        text-align: center;
        margin: 4rem 0;
      }

      .reveal-box {
        display: inline-block;
        padding: 2rem 4rem;
        border: 2px dashed var(--gold);
        border-radius: 20px;
        cursor: pointer;
      }

      /* BALLOONS */
      .balloon {
        position: fixed;
        bottom: -100px;
        width: 40px;
        height: 50px;
        border-radius: 50%;
        opacity: 0.6;
        animation: float 10s linear infinite;
        z-index: -1;
      }

      @keyframes float {
        to {
          transform: translateY(-120vh) rotate(20deg);
        }
      }

      /* FLOATING BUTTONS */
      .fab {
        position: fixed;
        bottom: 2rem;
        right: 2rem;
        width: 70px;
        height: 70px;
        border-radius: 50%;
        background: var(--pink);
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 2rem;
        cursor: pointer;
      }

      .music {
        right: 6.5rem;
      }

      /* OVERLAY */
      .overlay {
        position: fixed;
        inset: 0;
        background: rgba(0, 0, 0, 0.9);
        display: none;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        z-index: 9999;
      }
    </style>
    <link
      href="https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap"
      rel="stylesheet"
    />
  </head>

  <body>
    <div class="aurora-bg"></div>

    <!-- AUDIO -->
    <audio id="bgMusic" loop>
      <source src="videoplayback.weba" type="audio/mpeg" sound:80% />
    </audio>

    <!-- LANDING -->
    <section class="landing" id="landing">
      <div>
        <div class="subtitle">Happy Birthday to You!</div>
        <div class="date">
          ✨ Can't Wait till Magh-23 <br />
          <br />
          Wishing on MAGH SUKLA CHATURDASI.💌💝✨
        </div>
        <button class="btn" id="enterBtn">CLICK ME 🎁</button>
      </div>
    </section>

    <!-- MAIN -->
    <section class="main" id="main">
      <div class="container">
        <h2
          class="title"
          style="font-family: 'Indie Flower', cursive; color: #00f5ff"
        >
          HAPPY BIRTHDAY Tamatar
        </h2>

        <div class="cards">
          <div class="card">
            <div class="icon">🎂</div>
            <h3>The Occasion</h3>
            <p>
              Another Year! You are 14, another year of joy and emotions🧡💗 <br>

              <br>
              <p style="font-style: italic;">
                Remember:
              </p>
              <br>
              <p style="font-style: normal;">
               <li> The dance we did on Saraswati Puja 2076, </li> <br/> <br>
                <li>The ISA project we completed together, </li><br /> <br> 
               <li> The moment I taught you Scrabble on 2077, </li><br> <br>
               <li> The moment when you used to run in shyness back in 2076,</li> <br />  <br>
                <li>The time we spent together in past, </li> <br />
               <li> Ahh, the dance moment. Aaich! </li> <br> 
                </p>
                <p style="font-style: italic;">
                All are the memories I will cherish forever. <br />
              </p>
            </p>
          </div>
          <div class="card">
            <div class="icon">✨</div>
            <h3>Your Spark</h3>
            <p style="font-family: Garamond">
              The moon itself hides behind the cloud, <br />
              When it sees you smiling loud, <br />
              Today its the day to shine more bright, <br />
              Wishing you another year of pure delight. <br />
              <br />
              I am so grateful to say शुभकमाना जन्मदिनको. <br />
              You and your beauty are more than metaphor of moon को
            </p>
          </div>
          <div class="card">
            <div class="icon">🎊🫶</div>
            <h3>Wishes:</h3>
            <p>जन्मदिवसस्य शुभकामनाः! त्वं मे हृदयस्य प्रियतमः। <br /></p>
            <p>
              प्रार्थयामहे भव शतायुषी, ईश्वरः सदा त्वां च रक्षतु। <br />
              पुण्यकर्मणा कीर्तिमार्जय, जीवनं तव भवतु सार्थकम्।।
            </p>
          </div>
        </div>

        <div class="wish">
          <p>
            May your life be as beautiful as your heart,<br />
            and your smile never fade.
          </p>
        </div>

        <div class="reveal">
          <div class="reveal-box" id="revealBox">
            <span id="revealText">Click for a Birthday Secret 🤫</span>
          </div>
        </div>
      </div>
    </section>

    <!-- BUTTONS -->
    <div class="fab music" id="musicBtn">🎵</div>
    <div class="fab" id="partyBtn">🎉</div>

    <!-- OVERLAY -->
    <div class="overlay" id="overlay">
      <h1
        style="
          font-family: 'Playfair Display', serif;
          color: var(--pink);
          font-size: 3rem;
          text-align: center;
          margin: 0 auto;
        "
      >
        Once Again Happy Birthday 🎉
      </h1>

      <p style="margin: 20px; font-size: 1.5rem">❤️</p>
      <button class="btn" onclick="closeOverlay()">Back</button>
    </div>

    <script>
      const enterBtn = document.getElementById("enterBtn");
      const landing = document.getElementById("landing");
      const main = document.getElementById("main");
      const revealBox = document.getElementById("revealBox");
      const revealText = document.getElementById("revealText");
      const partyBtn = document.getElementById("partyBtn");
      const overlay = document.getElementById("overlay");

      const musicBtn = document.getElementById("musicBtn");
      const music = document.getElementById("bgMusic");
      let playing = false;

      /* AUTO PLAY AFTER 5 SECONDS (may be blocked until user clicks) */
      setTimeout(() => {
        music
          .play()
          .then(() => {
            playing = true;
            musicBtn.textContent = "⏸️";
          })
          .catch(() => {
            // autoplay blocked – user will start manually
          });
      }, 5000);

      // ENTER
      enterBtn.onclick = () => {
        landing.style.opacity = 0;
        setTimeout(() => {
          landing.style.display = "none";
          main.style.display = "block";
          setTimeout(() => (main.style.opacity = 1), 50);
          balloons();
        }, 1000);
      };

      // REVEAL
      const secrets = [
        "You're Prettiest!💖",
        "You're Amazing! ✨",
        "You're special for me🌸",
        "I'm glad I shared Special moments with you! 🎂",
      ];

      revealBox.onclick = () => {
        revealText.textContent =
          secrets[Math.floor(Math.random() * secrets.length)];
        revealText.style.color = "#ffd60a";
      };

      // MUSIC TOGGLE (PAUSE ↔ PLAY)
      musicBtn.onclick = () => {
        if (!playing) {
          music.play();
          musicBtn.textContent = "⏸️";
          playing = true;
        } else {
          music.pause();
          musicBtn.textContent = "🎵";
          playing = false;
        }
      };

      // BALLOONS
      function balloons() {
        setInterval(() => {
          const b = document.createElement("div");
          b.className = "balloon";
          b.style.left = Math.random() * 100 + "vw";
          b.style.background = ["#ff70a6", "#ffd60a", "#00f5ff", "#06ffa5"][
            Math.floor(Math.random() * 4)
          ];
          document.body.appendChild(b);
          setTimeout(() => b.remove(), 10000);
        }, 1500);
      }

      // PARTY
      partyBtn.onclick = () => {
        overlay.style.display = "flex";
        for (let i = 0; i < 50; i++) confetti();
      };

      function closeOverlay() {
        overlay.style.display = "none";
      }

      function confetti() {
        const c = document.createElement("div");
        c.style.position = "fixed";
        c.style.width = "10px";
        c.style.height = "10px";
        c.style.background = ["#ff70a6", "#ffd60a", "#00f5ff"][
          Math.floor(Math.random() * 3)
        ];
        c.style.left = Math.random() * 100 + "vw";
        c.style.top = "-10px";
        c.style.borderRadius = "50%";
        document.body.appendChild(c);

        c.animate(
          [
            { transform: "translateY(0)", opacity: 1 },
            {
              transform: `translateY(100vh) translateX(${
                Math.random() * 200 - 100
              }px) rotate(720deg)`,
              opacity: 0,
            },
          ],
          { duration: 3000 }
        ).onfinish = () => c.remove();
      }
    </script>
  </body>
</html>

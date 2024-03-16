🏗 WORK IN PROGRESS🚧
- 👋 Hi, I’m @Ludensburger
- ⚛ Currently Learning REACT
- 👀 I’m interested in C/C++, and Java
- 🌱 I’m currently learning JS & React
- 🤝 In collaboration with [Jaco](https://github.com/jacocanete)
- 💞️ I’m looking to collaborate on almost anything as long as its interesting and fun, that will help me in my Journey as a Programmer.
- 📫 How to reach me: You can shoot a DM in Instagram @ryu.bmth

<!---
Ludensburger/Ludensburger is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="shortcut icon" href="./icon.png" type="image/x-icon" />
    <!-- <link rel="stylesheet" href="style.css" /> -->

    <style>
      * {
        margin: 0px;
        padding: 0px;
        box-sizing: border-box;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      }

      .main {
        --high-opacity: 1;
        --low-opacity: 0.6;
        --spiral-height: 100px;
        --letter-gap: 10px;
        --animation-duration: 5s;
      }

      .main {
        background-color: #18032c;
        color: #ffffff;
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: 40px;
        text-transform: uppercase;
      }

      /* Custom Property */
      @property --angle {
        syntax: "<angle>";
        initial-value: 0deg;
        inherits: false;
      }

      .animated-span,
      .animated-span-2 {
        display: flex;
        align-items: center;
        gap: var(--letter-gap);
        position: absolute;
      }

      .animated-span span {
        display: inline-block;
        transform: translateY(calc(sin(var(--angle)) * var(--spiral-height)))
          scale(calc(cos(var(--angle)) * 0.5 + 0.5));
        animation: spiral var(--animation-duration) linear infinite;
      }

      .animated-span-2 span {
        display: inline-block;
        transform: translateY(calc(sin(var(--angle)) * var(--spiral-height)))
          scale(calc(cos(var(--angle)) * 0.5 + 0.5));
        animation: spiral var(--animation-duration) linear infinite;
      }

      @keyframes spiral {
        0% {
          --angle: 360deg;
          opacity: var(--high-opacity);
        }
        100% {
          --angle: 0deg;
          opacity: var(--low-opacity);
        }
      }
    </style>
    <title>Animation</title>
  </head>
  <body>
    <div class="main">
      <span class="animated-span-2">Ryu Mendoza</span>
      <span class="animated-span">Ryu Mendoza</span>
    </div>
    <script>
      // JS for first animated span
      const span = document.querySelector(".animated-span");
      const textContent = span.textContent;

      span.textContent = "";

      textContent.split("").forEach((letter, index) => {
        const spanForLetter = document.createElement("span");

        spanForLetter.textContent = letter;

        const delay = `-${index * (4000 / 16)}ms`;

        spanForLetter.style.animationDelay = delay;
        span.appendChild(spanForLetter);
      });

      // JS for second animated span
      const span2 = document.querySelector(".animated-span-2");
      const textContent2 = span2.textContent;

      span2.textContent = "";

      textContent2.split("").forEach((letter, index) => {
        const spanForLetter2 = document.createElement("span");

        spanForLetter2.textContent = letter;

        const delay = `-${index * (4000 / 16) + 2200}ms`;

        spanForLetter2.style.animationDelay = delay;
        span2.appendChild(spanForLetter2);
      });
    </script>
  </body>
</html>

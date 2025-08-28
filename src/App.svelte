<script>
  import "./app.css";
  import ProjectCard from "./lib/ProjectCard.svelte";

  let name = "Insharah Irfan Nazir";
  let bio =
    "I'm a Computer Science junior at FAST National University of Computer and Emerging Sciences interested in systems programming, game development, and data science. I'm always trying out new technologies and building projects that challenge me to think creatively about problem-solving. Turning complex problems into elegant code that sits at the intersection of technology and creativity is what I love to do.";

  let techStack = [
    "C++",
    "C",
    "Assembly",
    "SQL",
    "HTML/CSS",
    "JavaScript",
    "Svelte",
    "Python",
    "C#",
    ".NET",
    "SFML",
  ];

  let languages = [
    {
      name: "C++",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg",
      alt: "C++",
    },
    {
      name: "C",
      icon: "https://upload.wikimedia.org/wikipedia/commons/1/19/C_Logo.png",
      alt: "C Language",
    },
    {
      name: "Assembly",
      icon: "https://user-images.githubusercontent.com/103866722/177873824-ac727cae-29d5-406d-87de-93bb2bf21f02.png",
      alt: "Assembly Language",
    },
    {
      name: "SQL",
      icon: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Sql_data_base_with_logo.png/640px-Sql_data_base_with_logo.png",
      alt: "SQL",
    },
    {
      name: "HTML",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
      alt: "HTML5",
    },
    {
      name: "CSS",
      icon: "https://img.icons8.com/fluent/512/css3.png",
      alt: "CSS3",
    },
    {
      name: "JavaScript",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
      alt: "JavaScript",
    },
    {
      name: "Svelte",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg",
      alt: "Svelte",
    },
    {
      name: "Python",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
      alt: "Python",
    },
    {
      name: "C#",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg",
      alt: "C#",
    },
    {
      name: "MATLAB",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matlab/matlab-original.svg",
      alt: "MATLAB",
    },
    {
      name: "Shell Scripting",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg",
      alt: "Bash",
    },
  ];

  let tools = [
    {
      name: ".NET",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dotnetcore/dotnetcore-original.svg",
      alt: ".NET",
    },
    {
      name: "SFML",
      icon: "https://www.sfml-dev.org/images/logo.png",
      alt: "SFML",
    },
    {
      name: "Linux",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg",
      alt: "Linux",
    },
    {
      name: "MS SQL Server",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/microsoftsqlserver/microsoftsqlserver-plain.svg",
      alt: "MS SQL Server",
    },
    {
      name: "Git",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
      alt: "Git",
    },
    {
      name: "Docker",
      icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
      alt: "Docker",
    },
    {
      name: "ServiceNow",
      icon: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/ServiceNow_logo.svg/2560px-ServiceNow_logo.svg.png",
      alt: "ServiceNow",
    },
  ];

  let projects = [
    {
      title: "TravelEase",
      description:
        "A comprehensive travel booking system with 6 different views (Traveler, Admin, Tour Operator, Tour Guide, Hotel, Transport) with multiple interfaces integrated with personal analytics dashboards.",
      technologies: ["C#", ".NET", "SQL"],
      githubUrl: "https://github.com/insharahn/TravelEase",
      image: "/traveler.png",
      alt: "TravelEase screenshot of Traveler interface login",
    },
    {
      title: "Air Traffic Control System",
      description:
        "Real-time multithreaded airport traffic control system with runway scheduling, emergency handling, radar-based flight monitoring, and payment processing. 3 different processes, 1 big system.",
      technologies: ["C++", "Multithreading", "IPC"],
      githubUrl: "https://github.com/insharahn/Air-Traffic-Control-System",
      image: "/aircontrolx.png",
      alt: "Air Traffic Control System screenshot of main screen",
    },
    {
      title: "Data Storytelling - Home Equity",
      description:
        "Exploring the relationship between home equity and intergenerational wealth in Black families through a data-driven narrative and Scrollytelling.",
      technologies: ["Svelte", "Highcharts", "Data Visualization"],
      githubUrl: "https://github.com/insharahn/kwk-website",
      image: "/generational-gains.png",
      alt: "Data Storytelling - Home Equity screenshot of first section",
    },
    {
      title: "Plants vs. Zombies Recreation",
      description:
        "A recreation of the beloved PopCap Games classic built using C++ and SFML graphics library with custom game mechanics.",
      technologies: ["C++", "SFML", "OOP"],
      githubUrl: "https://github.com/insharahn/PVZ",
      image: "pvz-levels.png",
      alt: "Plants vs. Zombies Recreation screenshot of levels selection screen",
    },
    {
      title: "Leave Management System",
      description:
        "Built for ServiceNow, this Leave Management System automates leave requests, approvals, and tracking, streamlining HR processes and following ITSM principles.",
      technologies: ["ServiceNow", "JavaScript"],
      githubUrl: "https://github.com/insharahn/leave-management-system",
      image: "/lms.png",
      alt: "Leave Management System screenshot of xml file",
    },

    {
      title: "Centipede Game",
      description:
        "Atari's iconic arcade game Centipede recreated using C++ and SFML with authentic gameplay mechanics and retro aesthetics.",
      technologies: ["C++", "SFML"],
      githubUrl: "https://github.com/insharahn/Centipede",
      image: "/centipede.png",
      alt: "Centipede Game screenshot of game screen",
    },

    /*
    {
      title: "Zuma Recreated in Assembly",
      description:
        "The iconic game Zuma recreated using Assembly Language (MASM615 and Irvine32). A challenging project that showcases low-level programming skills.",
      technologies: ["Assembly", "MASM615"],
      githubUrl: "https://github.com/insharahn/Zuma-Recreated-in-Assembly",
      image: "zuma.png",
    },
    {
      title: "Notepad",
      description:
        "A console-based notepad/text editor where each character is a node in both a 4-dimensional Linked List i.e. with up, down, left, and right linkages (for inserting, backspace, entering, scrolling, etc.) and a Trie Tree (for searching and suggestions).",
      technologies: ["C++", "Data Structures"],
      githubUrl: "https://github.com/insharahn/4D-Linked-List-and-Tree-Notepad",
      image: "/notepad.png",
    },*/
  ];

  let funFacts = [
    "I prefer coding in the default gedit text editor in Ubuntu (in light mode) over any IDE, because that's how I learned programming.",
    "I was born in Songkhla, Thailand, but I don't remember anything about it.",
    "I am the first woman on my mother's side of the family in three direct generations to NOT become a doctor!",
    "Assembly was my favorite language to learn. I was heartbroken to find out it isn't wildly used.",
    "My family loves travelling and I've visited over 10 countries, but I hate airplanes.",
    "I've never broken a bone.",
    "My cat's name is Totoro. He's a gray Persian and the love of my life.",
    "I love reading manhwas and webnovels.",
  ];

  let displayedFact = funFacts[2]; // default fact

  function getRandomFact() {
    displayedFact = funFacts[Math.floor(Math.random() * funFacts.length)];
  }
</script>

<header>
  <ul class="header-menu">
    <li>♡</li>

    <li><a href="#about">About</a></li>
    <li>♡</li>
    <li><a href="#projects">Projects</a></li>
    <li>♡</li>

    <li><a href="https://github.com/insharahn" target="_blank">GitHub</a></li>
    <li>♡</li>

    <li>
      <a
        href="https://www.linkedin.com/in/insharah-irfan-nazir-a1903b247/"
        target="_blank">LinkedIn</a
      >
    </li>
    <li>♡</li>
  </ul>
</header>

<main class="portfolio">
  <section class="hero" id="about">
    <h1>Hi! I'm {name}</h1>
    <p class="hero-bio">{bio}</p>
    <p class="pronunciation">
      By the way, my name is pronounced insh-uh-ra, but I don't mind if you say
      it like insh-ra instead!
    </p>
  </section>

  <section class="tech-stack">
    <h2>Languages</h2>
    <div class="tech-grid">
      {#each languages as tech}
        <div class="tech-item">
          <img src={tech.icon} alt={tech.name} class="tech-icon" />
          <span class="tech-name">{tech.name}</span>
        </div>
      {/each}
    </div>

    <h2>Tools & Technologies</h2>
    <div class="tech-grid">
      {#each tools as tech}
        <div class="tech-item">
          <img src={tech.icon} alt={tech.name} class="tech-icon" />
          <span class="tech-name">{tech.name}</span>
        </div>
      {/each}
    </div>
  </section>

  <section class="projects-section" id="projects">
    <h2>Featured Projects</h2>
    <div class="projects-grid featured-grid">
      {#each projects as project}
        <ProjectCard {project} />
      {/each}
      <p class="projects-note">
        <a href="https://github.com/insharahn"
          >Check the rest out at my GitHub :D</a
        >
      </p>
    </div>
  </section>

  <section class="contact-section" id="contact">
    <h2>Get in Touch</h2>
    <p>
      Feel free to contact me about anything and I'll be sure to respond
      quickly!
    </p>

    <form
      action="https://formspree.io/f/xrbabndz"
      method="POST"
      class="contact-form"
    >
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="_replyto" placeholder="Your Email" required />
      <textarea name="message" placeholder="Your Message" rows="5" required
      ></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <aside class="fun-facts-aside">
    <div class="fun-facts-header">
      <button class="fact-btn" on:click={getRandomFact}>
        Click here to get a random fun fact about me!
      </button>
    </div>
    <div class="fun-facts-body">
      <img
        class="heart-img"
        src="https://static.vecteezy.com/system/resources/thumbnails/012/658/363/small/heart-shaped-love-icon-symbol-for-pictogram-app-website-logo-or-graphic-design-element-pixel-art-style-illustration-format-png.png"
        alt="pixel heart"
      />
      <p class="fun-fact-text">{displayedFact}</p>
    </div>
  </aside>
</main>

<footer>
  <p>
    Made with ❤️ by Insharah Irfan Nazir | <a
      href="mailto:insharahnazir@gmail.com">insharahnazir@gmail.com</a
    >
  </p>
  <p>2025</p>
</footer>

<style>
  .portfolio {
    padding: 20px;
    max-width: 1200px;
    margin: auto;
    text-align: left;
  }

  .hero {
    text-align: center;
    padding: 40px 0;
    margin-bottom: 40px;
  }

  .hero h1 {
    font-size: 3em;
    margin-bottom: 20px;
    color: #d55984;
  }

  .hero-bio {
    font-size: 1.2em;
    max-width: 800px;
    margin: 0 auto 15px auto;
    line-height: 1.6;
  }

  .pronunciation {
    font-style: italic;
    color: #d55984;
    margin-top: 10px;
    margin-bottom: 0px;
  }

  .tech-stack {
    margin: 50px 0;
    margin-top: 0px;
    justify-content: center;
  }

  .tech-stack h2 {
    margin-bottom: 25px;
  }

  .tech-stack h2:not(:first-child) {
    margin-top: 40px;
  }

  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
    justify-content: center;
    text-align: center;
  }

  .tech-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    background-color: #feede8;
    border: 1px solid #f5babe;
    border-radius: 15px;
    transition: all 0.3s ease;
    text-align: center;
  }

  .tech-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    border-color: #d55984;
    background-color: #f5babe;
  }

  .tech-icon {
    width: 50px;
    height: 50px;
    margin-bottom: 10px;
    object-fit: contain;
  }

  .tech-name {
    font-family: "Fira Mono", monospace;
    font-size: 0.9em;
    font-weight: 500;
    color: #34568f;
  }

  .projects-section {
    margin: 50px 0;
  }

  .projects-grid {
    display: grid;
    gap: 30px;
    margin-top: 30px;
  }

  .projects-note a {
    font-size: medium;
    font-style: italic;
    color: #d55984;
  }
  .projects-note a:hover {
    font-style: italic;
    color: #34568f;
  }

  .featured-grid {
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  }

  .contact-section {
    background-color: #feede8;
    padding: 40px;
    border-radius: 15px;
    border: 2px dashed #d55984;
    margin: 50px 0;
    text-align: center;
  }

  .contact-section h2 {
    color: #d55984;
    margin-bottom: 15px;
  }

  .contact-section p {
    margin-top: 10px;
    margin-bottom: 30px;
  }

  .contact-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    max-width: 500px;
    margin: 0 auto;
  }

  .contact-form input,
  .contact-form textarea {
    padding: 12px;
    border: 2px solid #d55984;
    border-radius: 10px;
    font-size: 1rem;
    outline: none;
    font-family: "Courier New", Courier, monospace;
  }

  .contact-form input:focus,
  .contact-form textarea:focus {
    border-color: #34568f;
  }

  .contact-form button {
    background-color: #d55984;
    color: white;
    font-weight: bold;
    padding: 12px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    transition: 0.2s;
  }

  .contact-form button:hover {
    background-color: #34568f;
  }

  /* mobile responsiveness */
  @media (max-width: 768px) {
    .hero h1 {
      font-size: 2.5em;
    }

    .featured-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

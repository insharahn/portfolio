<script>
  export let project; //project object with title, description, technologies, githubUrl, image prop
</script>

<div class="project-card">
  <div class="card-image">
    <img src={project.image} alt={project.title} />
    <div class="card-overlay">
      <a href={project.githubUrl} target="_blank" class="github-link">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
          <!--github svg logo-->
          <path
            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
          />
        </svg>
        View Code
      </a>
    </div>
  </div>
  <div class="card-content">
    <h3 class="project-title">{project.title}</h3>
    <p class="project-description">{project.description}</p>
    <div class="tech-tags">
      {#each project.technologies as tech}
        <span class="tech-tag">{tech}</span>
      {/each}
    </div>
  </div>
</div>

<style>
  .project-card {
    background-color: #feede8;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    border: 1px solid #f5babe;
  }

  .project-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
    border-color: #d55984;
  }

  .card-image {
    position: relative;
    height: 200px;
    overflow: hidden;
  }

  .card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
  }

  .project-card:hover .card-image img {
    transform: scale(1.05);
  }

  .card-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(213, 89, 132, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.3s ease;
  }

  .project-card:hover .card-overlay {
    opacity: 1;
  }

  .github-link {
    display: flex;
    align-items: center;
    gap: 8px;
    color: white;
    text-decoration: none;
    font-weight: 600;
    font-family: "Fira Mono", monospace;
    padding: 10px 20px;
    border: 2px solid white;
    border-radius: 25px;
    transition: all 0.2s ease;
  }

  .github-link:hover {
    background-color: white;
    color: #d55984;
  }

  .card-content {
    padding: 25px;
  }

  .project-title {
    color: #d55984;
    font-family: "Jost", sans-serif;
    font-size: 1.4em;
    margin: 0 0 12px 0;
    font-weight: 600;
  }

  .project-description {
    color: #34568f;
    line-height: 1.6;
    margin: 0 0 20px 0;
    font-size: 0.95em;
  }

  .tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tech-tag {
    background-color: #f5babe;
    color: #34568f;
    padding: 4px 12px;
    border-radius: 15px;
    font-family: "Fira Mono", monospace;
    font-size: 0.8em;
    font-weight: 500;
  }

  @media (max-width: 768px) {
    .card-image {
      height: 180px;
    }

    .card-content {
      padding: 20px;
    }

    .project-title {
      font-size: 1.2em;
    }
  }
</style>

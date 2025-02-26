---
layout: page
title: The Lab
permalink: /lab/
---

<div class="section-header lab">
  <div class="container">
    <h1>The Lab</h1>
    <p class="section-description">Experimental projects at the intersection of AI, architecture, and housing solutions.</p>
  </div>
</div>

<section class="section-intro">
  <div class="container">
    <p>
      The Lab is our experimental space where we explore innovative approaches to housing challenges. 
      Here we combine AI-assisted design, architectural prototypes, and urban planning simulations to 
      develop new solutions for supportive housing and urban interventions.
    </p>
    
    <p>
      Our projects range from conceptual explorations to practical implementations, always with 
      the goal of creating more effective, efficient, and humane housing solutions.
    </p>
  </div>
</section>

<section class="featured-project">
  <div class="container">
    <h2>Featured Project</h2>
    
    {% assign featured = site.lab | first %}
    {% if featured %}
    <div class="project-highlight">
      <h3><a href="{{ featured.url }}">{{ featured.title }}</a></h3>
      <p class="project-meta">{{ featured.date | date: "%b %-d, %Y" }}</p>
      <p>{{ featured.excerpt }}</p>
      <a href="{{ featured.url }}" class="read-more">Read More</a>
    </div>
    {% else %}
    <p>Featured projects coming soon.</p>
    {% endif %}
  </div>
</section>

<section class="projects-container">
  <div class="container">
    <h2>Projects</h2>
    
    <div class="categories-filter">
      <button class="filter-button active" data-filter="all">All</button>
      <button class="filter-button" data-filter="ai-design">AI & Design</button>
      <button class="filter-button" data-filter="housing-prototypes">Housing Prototypes</button>
      <button class="filter-button" data-filter="urban-simulation">Urban Simulation</button>
    </div>
    
    <div class="projects-grid">
      {% for project in site.lab %}
      <div class="project-card" data-category="{{ project.subcategory | default: 'other' }}">
        <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
        <p>{{ project.excerpt }}</p>
        <a href="{{ project.url }}" class="read-more">View Project</a>
      </div>
      {% endfor %}
      
      {% if site.lab.size == 0 %}
      <p>Projects coming soon. Check back later for updates.</p>
      {% endif %}
    </div>
  </div>
</section>

<section class="submit-idea">
  <div class="container">
    <h2>Have a Project Idea?</h2>
    <p>
      We're always looking for innovative approaches to housing challenges. If you have an idea 
      for a project or experiment, we'd love to hear from you.
    </p>
    <a href="/contact" class="button">Submit an Idea</a>
  </div>
</section>

<script>
  // Simple filter functionality for projects
  document.addEventListener('DOMContentLoaded', function() {
    const filterButtons = document.querySelectorAll('.filter-button');
    const projectCards = document.querySelectorAll('.project-card');
    
    filterButtons.forEach(button => {
      button.addEventListener('click', function() {
        const filter = this.getAttribute('data-filter');
        
        // Update active button
        filterButtons.forEach(btn => btn.classList.remove('active'));
        this.classList.add('active');
        
        // Filter projects
        projectCards.forEach(card => {
          if (filter === 'all' || card.getAttribute('data-category') === filter) {
            card.style.display = 'block';
          } else {
            card.style.display = 'none';
          }
        });
      });
    });
  });
</script>

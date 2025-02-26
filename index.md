---
layout: home
title: Urban Acupuncture Fund
---

<div class="hero">
  <div class="hero-content">
    <h1>Reimagining Urban Spaces</h1>
    <p class="tagline">Small interventions. Transformative impact.</p>
    <a href="/about" class="button">Learn More</a>
  </div>
</div>

<section class="intro">
  <div class="container">
    <h2>Urban Acupuncture: A New Paradigm</h2>
    <p>
      Urban acupuncture is a socio-environmental theory combining contemporary urban design with traditional Chinese acupuncture, using small-scale interventions to transform the larger urban context. At the Urban Acupuncture Fund, we explore how targeted interventions can address homelessness and housing challenges through innovative design, financing, and community engagement.
    </p>
  </div>
</section>

<section class="sections-preview">
  <div class="container">
    <div class="section-card lab">
      <h3>The Lab</h3>
      <p>Experimental projects at the intersection of AI, architecture, and housing solutions.</p>
      <a href="/lab" class="read-more">Explore</a>
    </div>
    
    <div class="section-card library">
      <h3>The Library</h3>
      <p>Case studies of successful interventions, research, and analysis resources.</p>
      <a href="/library" class="read-more">Explore</a>
    </div>
    
    <div class="section-card workshop">
      <h3>The Workshop</h3>
      <p>Practical guides for implementing supportive housing and community-led development.</p>
      <a href="/workshop" class="read-more">Explore</a>
    </div>
    
    <div class="section-card exchange">
      <h3>The Exchange</h3>
      <p>Models for blending public and private capital, innovative financing mechanisms.</p>
      <a href="/exchange" class="read-more">Explore</a>
    </div>
    
    <div class="section-card forum">
      <h3>The Forum</h3>
      <p>Interviews with practitioners, discussion spaces, and community dialogue.</p>
      <a href="/forum" class="read-more">Explore</a>
    </div>
  </div>
</section>

<section class="featured-content">
  <div class="container">
    <h2>Latest Insights</h2>
    
    <div class="featured-posts">
      {% for post in site.posts limit:3 %}
        <div class="featured-post">
          <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }} • {{ post.category }}</p>
          <p>{{ post.excerpt }}</p>
        </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="cta">
  <div class="container">
    <h2>Join The Conversation</h2>
    <p>Subscribe to receive updates on urban solutions, housing innovations, and funding opportunities.</p>
    
    <form action="#" method="post" class="signup-form">
      <input type="email" placeholder="Your email address" required>
      <button type="submit" class="button">Subscribe</button>
    </form>
  </div>
</section>

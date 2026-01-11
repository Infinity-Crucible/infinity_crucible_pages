---
layout: default
title: Home
---

<div class="hero">
  <img src="{{ '/assets/images/banner.png' | relative_url }}" alt="Infinity Crucible" class="hero-banner">
  <p class="hero-tagline">Quarters not required</p>
</div>

<section class="section">
  <h2 class="section-title">About the Game</h2>
  <p>
    You were an arrogant mage who thought you held the world in the palm of your hand.
    Then you were kidnapped by ogres and forced to perform in their infinite supply of
    monster-ridden dungeons, purely for their entertainment. Survive, or die trying, over and over again, because you can't seem to stay dead. Death offers no escape. Your ego won't allow it.
  </p>
  <p>
    Remember when arcades smelled like pizza and broken dreams? When "Elf needs food badly"
    was a legitimate crisis? Infinity Crucible is a love letter to those quarter-munching
    dungeon crawlers, rebuilt for the modern age with Godot 4 and Rust.
  </p>
  <p>
    Descend through procedurally generated dungeons. Smash spawners before they overwhelm you.
    Juggle spells, swap gear, grab powerups, and see how deep you can go before permadeath
    sends you back to level one. You know the drill.
  </p>
  <p>
    Currently in active development. Follow along as we figure out what we're doing.
  </p>

  <h3>Blame These Games</h3>
  <ul>
    <li><a href="https://en.wikipedia.org/wiki/Rogue_(video_game)">Rogue</a> (1980-ish)</li>
    <li><a href="https://en.wikipedia.org/wiki/Gateway_to_Apshai">Gateway to Apshai</a> (1983)</li>
    <li><a href="https://en.wikipedia.org/wiki/Gauntlet_(1985_video_game)">Gauntlet</a> (1985)</li>
    <li><a href="https://en.wikipedia.org/wiki/Brogue_(video_game)">Brogue</a> (2009)</li>
    <li><a href="https://en.wikipedia.org/wiki/Dark_Souls">Dark Souls</a> (2011)</li>
  </ul>
  <p>And so many others.</p>
</section>

<section class="section">
  <h2 class="section-title">Latest Updates</h2>

  {% for post in site.posts limit:3 %}
  <a href="{{ post.url | relative_url }}" class="card" style="display: block; text-decoration: none;">
    <h3 class="card-title">{{ post.title }}</h3>
    <time class="card-date">{{ post.date | date: "%B %d, %Y" }}</time>
    <p class="card-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
  </a>
  {% endfor %}

  {% if site.posts.size > 3 %}
  <a href="{{ '/updates' | relative_url }}" class="view-all">View all updates &rarr;</a>
  {% endif %}

  {% if site.posts.size == 0 %}
  <p class="card" style="color: #a1a1a1;">No updates yet. Check back soon!</p>
  {% endif %}
</section>

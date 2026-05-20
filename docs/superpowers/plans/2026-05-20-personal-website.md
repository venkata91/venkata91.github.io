# Personal Website Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the first version of a minimal, professional personal website for Venkata Krishnan Sowrirajan on GitHub Pages.

**Architecture:** Use plain static HTML and CSS with no build step. The homepage is a concise single-page profile with anchored sections, while `/blog/` starts as a lightweight placeholder page that shares the same styling.

**Tech Stack:** HTML5, CSS3, GitHub Pages static hosting, no JavaScript.

---

## File Structure

- Create: `index.html`
  - Primary homepage with semantic landmarks, hero, About, Projects, Talks & Blogs, Resume/CV, Links, and Blog sections.
- Create: `styles.css`
  - Shared responsive styling, typography, colors, layout, cards, links, and mobile behavior.
- Create: `blog/index.html`
  - Placeholder blog index that links back to the homepage and sets expectations for future writing.
- Modify: `.gitignore`
  - Already excludes `.superpowers/`; no new ignored generated files are required.

## Content Constants

Use these external links exactly:

- LinkedIn: `https://www.linkedin.com/in/venkatakrishnans/`
- GitHub: `https://github.com/venkata91`
- Apache Spark: `https://spark.apache.org/`
- Apache Flink: `https://flink.apache.org/`
- AlphaZero source: `https://github.com/venkata91/alphazero`
- AlphaZero docs: `https://venkata91.github.io/alphazero/`

Do not include a Twitter/X link unless the user supplies a handle.

### Task 1: Homepage HTML

**Files:**
- Create: `index.html`

- [ ] **Step 1: Create the homepage document**

Add this complete file:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Venkata Krishnan Sowrirajan</title>
    <meta
      name="description"
      content="Venkata Krishnan Sowrirajan is a data and AI infrastructure engineer working on distributed systems and open source projects including Apache Spark and Apache Flink."
    >
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <header class="site-header">
      <nav class="nav" aria-label="Primary navigation">
        <a class="brand" href="#top">Venkata Krishnan Sowrirajan</a>
        <div class="nav-links">
          <a href="#about">About</a>
          <a href="#projects">Projects</a>
          <a href="#talks-blogs">Talks &amp; Blogs</a>
          <a href="#resume">Resume/CV</a>
          <a href="blog/">Blog</a>
        </div>
      </nav>
    </header>

    <main id="top">
      <section class="hero" aria-labelledby="hero-title">
        <p class="eyebrow">Data &amp; AI Infrastructure · Distributed Systems · Open Source</p>
        <h1 id="hero-title">Building scalable data systems and open source infrastructure.</h1>
        <p class="hero-copy">
          I work on reliable distributed systems, compute infrastructure, and open source projects across
          Apache Spark, Apache Flink, Trino, and related data platforms.
        </p>
        <div class="link-row" aria-label="Primary links">
          <a href="https://www.linkedin.com/in/venkatakrishnans/">LinkedIn</a>
          <a href="https://github.com/venkata91">GitHub</a>
          <a href="blog/">Blog</a>
        </div>
      </section>

      <section id="about" class="section" aria-labelledby="about-title">
        <div class="section-heading">
          <p class="section-kicker">About</p>
          <h2 id="about-title">About me</h2>
        </div>
        <div class="section-body">
          <p>
            I enjoy building scalable and reliable distributed systems, with extensive experience working
            with Apache Spark, Apache Flink, Trino, and related infrastructure.
          </p>
          <p>
            Currently, I am leading an effort on compute convergence at LinkedIn using Apache Flink. I am
            passionate about contributing to open source and have contributed significantly to projects
            like Spark and Flink.
          </p>
          <p>
            If you are interested in distributed systems or open source, feel free to connect.
          </p>
        </div>
      </section>

      <section id="projects" class="section" aria-labelledby="projects-title">
        <div class="section-heading">
          <p class="section-kicker">Projects</p>
          <h2 id="projects-title">Selected work</h2>
        </div>
        <div class="project-list">
          <article class="project-card">
            <div>
              <h3>Apache Spark</h3>
              <p>
                Contributions to the open source unified engine for large-scale data analytics.
              </p>
            </div>
            <a href="https://spark.apache.org/" aria-label="Visit Apache Spark">Visit</a>
          </article>

          <article class="project-card">
            <div>
              <h3>Apache Flink</h3>
              <p>
                Contributions to the open source framework and distributed processing engine for stateful
                computations over bounded and unbounded data streams.
              </p>
            </div>
            <a href="https://flink.apache.org/" aria-label="Visit Apache Flink">Visit</a>
          </article>

          <article class="project-card">
            <div>
              <h3>AlphaZero from Scratch</h3>
              <p>
                A personal Python and PyTorch learning project implementing a game-agnostic
                AlphaZero-style framework with docs and experiments.
              </p>
            </div>
            <div class="project-links">
              <a href="https://github.com/venkata91/alphazero">Source</a>
              <a href="https://venkata91.github.io/alphazero/">Docs</a>
            </div>
          </article>
        </div>
      </section>

      <section id="talks-blogs" class="section" aria-labelledby="talks-blogs-title">
        <div class="section-heading">
          <p class="section-kicker">Talks &amp; Blogs</p>
          <h2 id="talks-blogs-title">Writing and notes</h2>
        </div>
        <div class="section-body">
          <p>
            This section will collect talks, technical notes, and longer writing on distributed systems,
            open source development, and useful engineering hacks.
          </p>
          <a class="text-link" href="blog/">Go to the blog</a>
        </div>
      </section>

      <section id="resume" class="section" aria-labelledby="resume-title">
        <div class="section-heading">
          <p class="section-kicker">Resume/CV</p>
          <h2 id="resume-title">Resume</h2>
        </div>
        <div class="section-body">
          <p>
            A downloadable resume/CV can be added here later. For now, LinkedIn has the most current
            professional summary.
          </p>
          <a class="text-link" href="https://www.linkedin.com/in/venkatakrishnans/">View LinkedIn profile</a>
        </div>
      </section>

      <section id="links" class="section compact-section" aria-labelledby="links-title">
        <div class="section-heading">
          <p class="section-kicker">Links</p>
          <h2 id="links-title">Find me online</h2>
        </div>
        <div class="link-row">
          <a href="https://www.linkedin.com/in/venkatakrishnans/">LinkedIn</a>
          <a href="https://github.com/venkata91">GitHub</a>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <p>&copy; 2026 Venkata Krishnan Sowrirajan.</p>
    </footer>
  </body>
</html>
```

- [ ] **Step 2: Check the file exists**

Run: `test -f index.html && sed -n '1,40p' index.html`

Expected: command exits 0 and prints the document header, title, meta description, and stylesheet link.

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "Add personal website homepage"
```

### Task 2: Shared Styling

**Files:**
- Create: `styles.css`

- [ ] **Step 1: Create the stylesheet**

Add this complete file:

```css
:root {
  color-scheme: light;
  --bg: #f8fafc;
  --panel: #ffffff;
  --text: #172033;
  --muted: #5d687a;
  --line: #d9e0ea;
  --accent: #0f766e;
  --accent-strong: #115e59;
  --max-width: 1040px;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  line-height: 1.6;
}

a {
  color: var(--accent);
  text-decoration: none;
}

a:hover,
a:focus {
  color: var(--accent-strong);
  text-decoration: underline;
}

.site-header {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(248, 250, 252, 0.94);
  border-bottom: 1px solid var(--line);
  backdrop-filter: blur(12px);
}

.nav,
main,
.site-footer {
  width: min(var(--max-width), calc(100% - 40px));
  margin: 0 auto;
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  min-height: 64px;
}

.brand {
  color: var(--text);
  font-weight: 700;
}

.nav-links {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  justify-content: flex-end;
  font-size: 0.94rem;
}

.nav-links a {
  color: var(--muted);
}

.hero {
  padding: 96px 0 72px;
  border-bottom: 1px solid var(--line);
}

.eyebrow,
.section-kicker {
  margin: 0 0 10px;
  color: var(--accent-strong);
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0;
  text-transform: uppercase;
}

h1,
h2,
h3,
p {
  overflow-wrap: anywhere;
}

h1 {
  max-width: 820px;
  margin: 0;
  font-size: clamp(2.4rem, 6vw, 4.4rem);
  line-height: 1.05;
  letter-spacing: 0;
}

.hero-copy {
  max-width: 720px;
  margin: 24px 0 0;
  color: var(--muted);
  font-size: 1.16rem;
}

.link-row {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 28px;
}

.link-row a,
.text-link,
.project-card > a,
.project-links a {
  display: inline-flex;
  align-items: center;
  min-height: 40px;
  border-bottom: 1px solid currentColor;
  font-weight: 700;
}

.section {
  display: grid;
  grid-template-columns: minmax(180px, 260px) 1fr;
  gap: 48px;
  padding: 64px 0;
  border-bottom: 1px solid var(--line);
}

.section-heading h2 {
  margin: 0;
  font-size: 1.45rem;
  line-height: 1.25;
}

.section-body {
  max-width: 720px;
}

.section-body p {
  margin: 0 0 18px;
  color: var(--muted);
  font-size: 1.02rem;
}

.section-body p:last-child {
  margin-bottom: 0;
}

.project-list {
  display: grid;
  gap: 16px;
}

.project-card {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 24px;
  padding: 22px;
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: 8px;
}

.project-card h3 {
  margin: 0 0 8px;
  font-size: 1.08rem;
}

.project-card p {
  margin: 0;
  color: var(--muted);
}

.project-links {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  flex: 0 0 auto;
}

.compact-section {
  border-bottom: 0;
}

.compact-section .link-row {
  margin-top: 0;
}

.site-footer {
  padding: 36px 0 48px;
  color: var(--muted);
  font-size: 0.94rem;
}

.site-footer p {
  margin: 0;
}

@media (max-width: 760px) {
  .nav,
  main,
  .site-footer {
    width: min(100% - 28px, var(--max-width));
  }

  .nav {
    align-items: flex-start;
    flex-direction: column;
    gap: 10px;
    padding: 14px 0;
  }

  .nav-links {
    justify-content: flex-start;
    gap: 10px 14px;
  }

  .hero {
    padding: 64px 0 48px;
  }

  .section {
    grid-template-columns: 1fr;
    gap: 18px;
    padding: 46px 0;
  }

  .project-card {
    flex-direction: column;
    gap: 14px;
  }

  .project-links {
    flex: none;
  }
}
```

- [ ] **Step 2: Check CSS for dominant color drift and syntax basics**

Run: `rg -n "#|var\\(|@media|clamp|letter-spacing" styles.css`

Expected: output shows the neutral palette, one teal accent family, responsive media query, `clamp()` on the hero heading only, and `letter-spacing: 0`.

- [ ] **Step 3: Commit**

```bash
git add styles.css
git commit -m "Add minimal personal site styling"
```

### Task 3: Blog Placeholder

**Files:**
- Create: `blog/index.html`

- [ ] **Step 1: Create the blog index**

Add this complete file:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Blog | Venkata Krishnan Sowrirajan</title>
    <meta
      name="description"
      content="Technical notes and writing by Venkata Krishnan Sowrirajan on distributed systems, open source, and engineering."
    >
    <link rel="stylesheet" href="../styles.css">
  </head>
  <body>
    <header class="site-header">
      <nav class="nav" aria-label="Primary navigation">
        <a class="brand" href="../">Venkata Krishnan Sowrirajan</a>
        <div class="nav-links">
          <a href="../#about">About</a>
          <a href="../#projects">Projects</a>
          <a href="../#talks-blogs">Talks &amp; Blogs</a>
          <a href="../#resume">Resume/CV</a>
        </div>
      </nav>
    </header>

    <main>
      <section class="hero" aria-labelledby="blog-title">
        <p class="eyebrow">Blog</p>
        <h1 id="blog-title">Notes on systems, open source, and engineering practice.</h1>
        <p class="hero-copy">
          This space will collect longer-form notes, interesting hacks, and thoughts from working on
          distributed systems and data infrastructure.
        </p>
        <div class="link-row">
          <a href="../">Back to homepage</a>
          <a href="https://github.com/venkata91">GitHub</a>
        </div>
      </section>

      <section class="section compact-section" aria-labelledby="posts-title">
        <div class="section-heading">
          <p class="section-kicker">Posts</p>
          <h2 id="posts-title">Coming soon</h2>
        </div>
        <div class="section-body">
          <p>
            The first posts will be added here as standalone pages or migrated into a static blog engine
            when the writing archive grows.
          </p>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <p>&copy; 2026 Venkata Krishnan Sowrirajan.</p>
    </footer>
  </body>
</html>
```

- [ ] **Step 2: Check relative links**

Run: `rg -n "href=\"(\\.\\./|https://)" blog/index.html`

Expected: output shows stylesheet, homepage anchor links, homepage link, and GitHub link using the correct relative paths.

- [ ] **Step 3: Commit**

```bash
git add blog/index.html
git commit -m "Add blog placeholder page"
```

### Task 4: Static Validation

**Files:**
- Validate: `index.html`
- Validate: `blog/index.html`
- Validate: `styles.css`

- [ ] **Step 1: Inspect all internal site links**

Run: `rg -n "href=\"(#|blog/|\\.\\./|\\.\\./#)" index.html blog/index.html`

Expected: homepage anchors point to existing section IDs, `blog/` points to `blog/index.html`, and blog page links use `../` or `../#...`.

- [ ] **Step 2: Verify section IDs exist**

Run: `rg -n "id=\"(top|about|projects|talks-blogs|resume|links|hero-title|blog-title|posts-title)\"" index.html blog/index.html`

Expected: output includes all homepage section IDs and blog page heading IDs referenced by `aria-labelledby`.

- [ ] **Step 3: Serve locally**

Run: `python3 -m http.server 8000`

Expected: server starts with a line like `Serving HTTP on :: port 8000` or `Serving HTTP on 0.0.0.0 port 8000`.

- [ ] **Step 4: Manually check pages in browser**

Open:

- `http://localhost:8000/`
- `http://localhost:8000/blog/`

Expected:

- Desktop layout is readable and professional.
- Mobile-width layout stacks cleanly.
- Header links navigate to the expected sections.
- Blog page loads the shared stylesheet.
- External links point to LinkedIn, GitHub, Apache Spark, Apache Flink, and AlphaZero.

- [ ] **Step 5: Stop the local server**

Press `Ctrl-C` in the terminal running `python3 -m http.server 8000`.

- [ ] **Step 6: Commit any validation fixes**

If validation required fixes, run:

```bash
git add index.html blog/index.html styles.css
git commit -m "Fix static site validation issues"
```

Expected: if no fixes were needed, skip this commit and record that validation passed without changes.

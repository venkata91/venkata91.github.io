# Personal Website Design

## Purpose

Create a minimal, professional personal website for Venkata Krishnan Sowrirajan at this GitHub Pages repository. The first version should communicate a clear identity: data and AI infrastructure engineer, distributed systems builder, and open source contributor.

The site should be simple enough to maintain by editing static files directly, while leaving room to evolve into a richer blog or generated static site later.

## Scope

Version 1 includes:

- A single-page homepage with anchored sections.
- A placeholder blog index at `/blog/`.
- Links to LinkedIn, GitHub, and Twitter/X when available.
- Project links for Apache Spark, Apache Flink, and AlphaZero.
- A Resume/CV section that can remain optional for now.

Version 1 does not include:

- A full blog engine.
- Generated RSS feeds, tags, categories, or search.
- A JavaScript framework or build pipeline.
- Detailed resume content beyond an optional placeholder link.

## Architecture

Use plain static HTML and CSS:

- `index.html`: homepage and primary profile.
- `styles.css`: shared site styling.
- `blog/index.html`: placeholder blog landing page.

The site has no build step and should be directly compatible with GitHub Pages. Shared visual language comes from one stylesheet rather than a component framework.

## Homepage Structure

The homepage uses a concise single-page profile layout:

1. Header navigation with anchors for About, Projects, Talks & Blogs, Resume/CV, and Blog.
2. Hero section with name, professional positioning, and primary social links.
3. About section using the supplied LinkedIn About copy, lightly edited for website voice.
4. Projects section with selected project rows/cards:
   - Apache Spark
   - Apache Flink
   - AlphaZero
5. Talks & Blogs section with a lightweight placeholder for future entries.
6. Resume/CV section marked optional, with copy that can later point to a PDF.
7. Links/contact section with LinkedIn, GitHub, and Twitter/X links as available.

## Content

The About section should be based on this user-supplied source text:

> I enjoy building scalable and reliable distributed systems, and have extensive experience working with Apache Spark, Apache Flink, Trino, and more.
>
> Currently, I'm leading an effort on compute convergence at LinkedIn using Apache Flink. I am passionate about contributing to open-source projects and have contributed significantly to projects like Spark and Flink.
>
> If you're interested in distributed systems or open source, feel free to connect with me!

The first website draft may lightly edit this for flow, but should preserve the meaning and avoid adding unverified claims.

Project descriptions should stay conservative:

- Apache Spark: open source unified engine for large-scale data analytics.
- Apache Flink: open source framework and distributed processing engine for stateful computations over bounded and unbounded data streams.
- AlphaZero: personal Python/PyTorch learning project implementing a game-agnostic AlphaZero-style framework, with docs and experiments.

## Styling

The visual style should be minimal, simple, and professional:

- Neutral background.
- High-contrast readable text.
- One restrained accent color for links and section markers.
- Narrow content width for readability.
- Consistent spacing and typography.
- Lightweight cards or rows for projects, with no decorative-heavy hero.
- Responsive layout for mobile and desktop.

The site should avoid heavy animation, large marketing-style sections, and framework-specific visual clutter.

## Links

Known links for v1:

- LinkedIn: `https://www.linkedin.com/in/venkatakrishnans/`
- GitHub: `https://github.com/venkata91`
- AlphaZero: `https://github.com/venkata91/alphazero`
- AlphaZero docs: `https://venkata91.github.io/alphazero/`
- Apache Spark: `https://spark.apache.org/`
- Apache Flink: `https://flink.apache.org/`

Twitter/X should be included only if a handle is known. If it is not known during implementation, leave it out rather than using a placeholder URL.

## Validation

Validation for v1 should include:

- Open the static site locally or via a simple local server.
- Check desktop and mobile viewport layout.
- Confirm navigation anchors work.
- Confirm external links are correct.
- Confirm the page has semantic landmarks and accessible link text.
- Confirm the site works without JavaScript.

## Future Evolution

If the blog becomes active, the site can later migrate to Jekyll, Astro, or another static generator. The initial file structure should keep content and styling simple enough that such a migration is straightforward.

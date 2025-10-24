Build in Public Hackathon — Landing Page (for Claude Code)
Goal

Create a single-file, static landing page for the Build in Public Hackathon (NYC). Minimal, fast, deployable to Vercel with no backend. Primary CTA: collect interested emails via Google Form (preferred) or mailto: fallback.

Tech/Constraints

One file: index.html (+ optional favicon.ico)

Tailwind via CDN for styling; a few lines of vanilla JS

Email capture posts to a Google Form (replace placeholders)

Works without JS (progressive enhancement)

Mobile-first; good OG/Twitter meta for sharing

File Structure
/ (project root)
 ├─ index.html
 └─ favicon.ico   (optional)

Replace-me Variables (put near top in a comment)

GOOGLE_FORM_ACTION_URL = "https://docs.google.com/forms/d/e/<FORM_ID>/formResponse"

GOOGLE_FORM_EMAIL_ENTRY_ID = "entry.<NUM>" (the email field entry id)

Tip to user: Create a Google Form named “Build in Public Hackathon — Interest List” with one Email question. Click “Get pre-filled link” → inspect network or “view source” after previewing to find formAction and the entry.xxxxxx id.

Page Sections & Copy

Hero

Title: Build in Public Hackathon — NYC

Sub: PMs × Engineers build AI-powered prototypes in one afternoon. We document everything—from idea → MVP → pitch.

Details line: Midtown NYC • Target: next month • ~30 builders

CTA button: Join the interest list

Logos (optional placeholders)

“Seen from” gray row (Meta, Google, Amazon, NYU, Columbia – label as “attendee backgrounds expected”, not official sponsors)

What it is

1-paragraph: One-afternoon hackathon where PMs from Meta/Google/Amazon pair with engineers from NYU & Columbia. Use tools like Claude, Perplexity, Vercel, Figma, Supabase to ship a demo in ~4 hours. We film highlights and publish across LinkedIn/YouTube.

Schedule

1:00–1:30 Check-in + intros

1:30–2:15 PM idea pitches (3 min each)

2:15–2:30 Team formation

2:30–6:15 Build sprint (AI-assisted)

6:15–7:15 Final demos & judging

7:15–8:00 Awards + networking

Who should attend

Working PMs who can scope a 4-hour MVP

Engineers/Designers (NYU/Columbia and beyond) who love fast prototyping

Judging (tentative)

Clarity of problem • Product value & UX • Execution creativity • Storytelling

Sponsors / Partners (open)

Looking to highlight AI/dev tools via credits, swag, or a judge

FAQ (short)

Cost: Free/invite-only

Code/IP: Yours

Tools: Any (Claude, Perplexity, Vercel recommended)

Footer

Contact: kyle [at] yourdomain.com • Social links

Small privacy note: “We only use your email to share event details and recap.”

Accessibility/SEO

Semantic tags, labels on inputs, focus states

Meta title/description

Open Graph + Twitter cards (use a neutral preview image if available)

Minimal HTML (Claude: generate exactly this with placeholders filled)
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Build in Public Hackathon — NYC</title>
  <meta name="description" content="PMs and engineers co-build AI prototypes in one afternoon. Documented from idea → MVP → pitch. Join the interest list." />
  <meta property="og:title" content="Build in Public Hackathon — NYC">
  <meta property="og:description" content="PMs and engineers co-build AI prototypes in one afternoon. We film highlights and share across LinkedIn & YouTube.">
  <meta property="og:type" content="website">
  <meta property="og:image" content="/og.jpg">
  <meta name="twitter:card" content="summary_large_image">
  <link rel="icon" href="/favicon.ico">
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Replace these with your real values -->
  <script>
    window.GOOGLE_FORM_ACTION_URL = "REPLACE_WITH_GOOGLE_FORM_ACTION_URL";
    window.GOOGLE_FORM_EMAIL_ENTRY_ID = "REPLACE_WITH_entry_xxxxx";
  </script>
</head>
<body class="bg-zinc-50 text-zinc-900">
  <header class="max-w-5xl mx-auto px-4 py-12">
    <div class="text-center">
      <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight">Build in Public Hackathon — NYC</h1>
      <p class="mt-4 text-lg sm:text-xl text-zinc-600">PMs × Engineers build AI-powered prototypes in one afternoon. We document everything—from idea → MVP → pitch.</p>
      <p class="mt-2 text-sm text-zinc-500">Midtown NYC • next month • ~30 builders</p>
      <a href="#interest" class="inline-block mt-6 px-6 py-3 bg-black text-white rounded-xl hover:opacity-90 focus:ring-2 focus:ring-offset-2 focus:ring-black">Join the interest list</a>
    </div>
  </header>

  <main class="max-w-5xl mx-auto px-4 space-y-16 pb-24">
    <section class="grid sm:grid-cols-2 gap-8">
      <div class="bg-white p-6 rounded-2xl shadow-sm">
        <h2 class="text-xl font-semibold">What it is</h2>
        <p class="mt-3 text-zinc-600">
          One-afternoon hackathon pairing <strong>PMs from Meta, Google, and Amazon</strong> with
          <strong>engineers from NYU & Columbia</strong>. Teams use tools like <strong>Claude, Perplexity, Vercel, Figma, Supabase</strong> to ship a demo in ~4 hours.
          Highlights published across LinkedIn & YouTube.
        </p>
      </div>
      <div class="bg-white p-6 rounded-2xl shadow-sm">
        <h2 class="text-xl font-semibold">Schedule</h2>
        <ul class="mt-3 text-zinc-600 space-y-1">
          <li><strong>1:00–1:30</strong> Check-in + intros</li>
          <li><strong>1:30–2:15</strong> PM idea pitches</li>
          <li><strong>2:15–2:30</strong> Team formation</li>
          <li><strong>2:30–6:15</strong> Build sprint (AI-assisted)</li>
          <li><strong>6:15–7:15</strong> Demos & judging</li>
          <li><strong>7:15–8:00</strong> Awards + networking</li>
        </ul>
      </div>
      <div class="bg-white p-6 rounded-2xl shadow-sm">
        <h2 class="text-xl font-semibold">Who should attend</h2>
        <p class="mt-3 text-zinc-600">Working PMs who can scope a 4-hour MVP. Engineers/Designers who love fast prototyping & AI workflows.</p>
      </div>
      <div class="bg-white p-6 rounded-2xl shadow-sm">
        <h2 class="text-xl font-semibold">Judging</h2>
        <p class="mt-3 text-zinc-600">Clarity of problem • Product value & UX • Execution creativity • Storytelling.</p>
      </div>
    </section>

    <section id="interest" class="bg-white p-6 rounded-2xl shadow-sm">
      <h2 class="text-xl font-semibold">Join the interest list</h2>
      <p class="mt-2 text-zinc-600">We’ll only email event details & recap. No spam.</p>

      <!-- Works without JS: direct POST to Google Form -->
      <form id="interestForm" class="mt-4 flex flex-col sm:flex-row gap-3"
            method="POST" target="_blank">
        <input required type="email" name="email"
               placeholder="your@email.com"
               class="w-full sm:flex-1 px-4 py-3 rounded-xl border border-zinc-300 focus:outline-none focus:ring-2 focus:ring-black" />
        <button class="px-6 py-3 rounded-xl bg-black text-white hover:opacity-90 focus:ring-2 focus:ring-offset-2 focus:ring-black">
          Notify me
        </button>
      </form>

      <p class="mt-3 text-xs text-zinc-500">
        Having trouble? Email <a class="underline" href="mailto:YOUR_EMAIL_HERE?subject=Hackathon%20Interest">YOUR_EMAIL_HERE</a>.
      </p>
    </section>

    <section class="text-sm text-zinc-500">
      <p>Looking to sponsor or judge? We’re highlighting AI/dev tools via credits, swag, or a panel spot. Contact: YOUR_EMAIL_HERE.</p>
    </section>
  </main>

  <footer class="py-10 text-center text-sm text-zinc-500">
    © <span id="y"></span> Build in Public Hackathon — NYC • Privacy: we only use your email for event updates.
  </footer>

  <script>
    document.getElementById('y').textContent = new Date().getFullYear();
    // Progressive enhancement: wire the form to Google Forms with correct field name
    const f = document.getElementById('interestForm');
    if (window.GOOGLE_FORM_ACTION_URL && window.GOOGLE_FORM_EMAIL_ENTRY_ID) {
      f.setAttribute('action', window.GOOGLE_FORM_ACTION_URL);
      // Replace visible input name with Google Forms entry id for POST
      const emailInput = f.querySelector('input[name="email"]');
      emailInput.setAttribute('name', window.GOOGLE_FORM_EMAIL_ENTRY_ID);
    }
  </script>
</body>
</html>

Deployment Steps (Vercel)

Create a new Git repo with index.html.

Replace the two Google Form placeholders and YOUR_EMAIL_HERE.

Push to GitHub → Vercel → New Project → Import. (Or drag-and-drop in Vercel.)

Set a pretty domain; upload favicon.ico if you have it.

Success Criteria

Loads fast on mobile; Lighthouse ≥ 90

Email submit opens Google “response recorded” screen in a new tab

Form works with JS and without JS

Clear CTA above the fold; content matches sections above


🧠 Event Specification — Build in Public Hackathon (NYC)
🎯 Purpose

The Build in Public Hackathon is a one-afternoon event designed to bring together Product Managers (PMs) and Engineers to co-build AI-powered prototypes in real time.
Participants will:

Take an idea from concept → prototype → pitch within 4–5 hours.

Leverage modern AI tools (Claude, Perplexity, Vercel, Figma, Supabase, etc.) to accelerate their workflow.

Be documented throughout the event, with highlights shared across LinkedIn, YouTube, and TikTok, showcasing how builders use AI to go from 0→1 in hours.

The spirit: collaboration, creativity, and transparency — building in public to inspire the next wave of AI product creation.

📅 Event Details

Date: Friday, November 22, 2025

Time: 1:00 PM – 8:00 PM EST

Location: WeWork Midtown NYC (exact address TBD)

Format: In-person, one-day sprint

Agenda:

1:00–1:30 — Check-in & networking

1:30–2:15 — PMs pitch product ideas (3 min each)

2:15–2:30 — Team formation

2:30–6:15 — Build sprint (AI-assisted prototyping)

6:15–7:15 — Final demos & judging

7:15–8:00 — Awards & networking mixer

👥 Participants

Product Managers (5–10):
From companies like Meta, Google, Amazon, and startups across NYC.
Each PM brings a product idea or challenge to lead during the build session.

Engineers / Designers (10–15):
From universities like NYU, Columbia, and Cornell Tech, and early-career startup builders.
They’ll join PMs to design, code, and present prototypes.

Judges / Mentors (3–5):
VCs, founders, and product leaders from the NYC tech community.
They’ll evaluate teams based on:

Clarity of problem

Product usefulness

Execution creativity

Storytelling during demo

Audience / Guests:
Around 30–35 total attendees, including sponsors and community members.
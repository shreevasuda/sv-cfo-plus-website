# SV CFO Plus — website

Four pages. Each one is **completely self-contained** — the CSS, the JavaScript, the logo and the
team photographs are all inside the HTML file. Upload the four files to any host and the site works.
Nothing to link up, no broken paths, no build step.

| File | Page |
|---|---|
| `index.html` | Home |
| `about.html` | Who We Are |
| `services.html` | Services |
| `contact.html` | Contact Us |
| `assets/` | Logo variants and the two team photographs, for reuse on letterheads, LinkedIn, proposals |

---

## What was changed from the previous version

**Rebranded throughout to SV CFO Plus.** Every reference to Vasuda Business Services is gone. The
site now reads "SV CFO Plus — A Unit of Shree Vasuda Venture Private Limited" and carries the
tagline *The Team Empowering Your Business* and the service line *Accounting · Finance · MIS ·
Virtual CFO · Business Support*.

**Your new logo, in four versions.** I trimmed the supplied artwork (it had a white background that
would have shown as a box) and built a horizontal lockup for the header, a white knockout version
for the dark footer, a mark-only version for the hero and favicon, and kept the full stacked lockup.
All are in `assets/` as transparent PNGs.

**Colours now follow the logo.** Blue leads (from "SV"), green and gold support it (from "CFO" and
"Plus"), which is why the site looks different from the last one.

**Real contact details from your letterhead** — both office addresses, phone, email and CIN, in the
top bar, the footer and the contact page.

**Founding members: degrees only, no write-ups.** All the prose has been removed as you asked.

| | |
|---|---|
| **Mr. Nikhil Chouhan** | Founding Member — MBA (Finance & Operations) |
| **CA Akhil Chauhan** | Founding Member — Chartered Accountant · Cost and Management Accountant · FRM (GARP) · **Ex-Banker** |

"Banker" is now "Ex-Banker" everywhere it appears.

**Who We Are, Vision and Mission are unchanged**, as you confirmed those were fine.

**The mentor panel stays as four qualified Chartered Accountants**, described by area of expertise
rather than named, with names offered privately on request.

---

## On readability and the "AI look"

Body text is **18px** with generous line spacing; nothing on the site sits below 16px. Headings are
in Poppins and body text in Source Sans 3 — both common, plainly readable typefaces you will
recognise from ordinary business websites rather than design showcases.

The structure follows the reference site: a coloured contact bar across the top, a small coloured
label above each section heading, round-cornered cards with icons and soft shadows, a stats band,
numbered work-process boxes, a team grid with real photographs, an FAQ accordion and a normal
contact block. Buttons are pill-shaped with plain labels — "Talk to Our Team", "Explore Our
Services", "Read More About Us".

The single biggest thing keeping it from looking generated is the real photographs of both founding
members. Adding client logos and testimonials (below) will push it further.

---

## Before you publish

**1. Check the two office addresses.** Taken from the letterhead:

- **Surat:** B-408, 4th Floor, Ambrosia Business Hub, Near Nandini-3, VIP Road, Vesu, Surat,
  Gujarat – 395007
- **Registered:** 2218, Solus Building, Hiranandani Estate, Opp. Bayer House, Thane (W), Mumbai,
  Maharashtra – 400 607

One of the drafts I was given wrote the Thane address as "B-2218" and another as "2218". I have used
**2218**. Please confirm against the letterhead.

**2. Get a domain email.** The site currently shows `shreevasudaventure@gmail.com` because that is
what the letterhead carries. A Gmail address costs you credibility with exactly the overseas clients
you are targeting — `info@svcfoplus.com` or similar is worth doing before this goes live.

**3. The CIN reads `U70200MR2026PTC479105`.** The state segment is **MR** where Maharashtra
companies normally carry **MH**. It is in the footer of all four pages. Please check it against the
Certificate of Incorporation — I have flagged this before and it is still worth ten minutes.

**4. Hours.** I have written "Monday to Saturday, 10:00 to 19:00 IST" on the contact page. Change it
if that is wrong.

**5. The "4 CAs" figure** appears in the stats band on the home page. Keep it accurate if the mentor
panel changes.

---

## Adding testimonials and client logos

These are the strongest trust elements on a site of this kind and the reference site leans on them
heavily. I have not invented any. When you have two or three real quotes with permission, this drops
straight into `index.html` immediately before `<section class="cta">`:

```html
<section class="wash">
  <div class="wrap">
    <div class="sec-head c reveal">
      <p class="eyebrow">Testimonials</p>
      <h2>What Our Clients Say</h2>
    </div>
    <div class="grid g3 reveal">
      <div class="card">
        <p>"The client's own words, unedited."</p>
        <p style="margin:18px 0 0"><b>Client Name</b><br>
        <span class="small muted">Title, Company</span></p>
      </div>
      <!-- repeat for each testimonial -->
    </div>
  </div>
</section>
```

---

## Hosting and the enquiry form

**Hosting:** drag the folder onto **netlify.com/drop** — live in under a minute, free, then point
your domain at it. Cloudflare Pages and GitHub Pages work the same way. On a cPanel host, upload the
files into `public_html`.

**The form** currently opens the visitor's own email application with the message pre-filled. That
works everywhere and stores nothing, but a fair share of mobile visitors abandon it. For a form that
lands in your inbox, sign up free at **formspree.io** or **web3forms.com**, then in `contact.html`
change:

```html
<form id="enquiry" novalidate>
```
to
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

and delete `id="enquiry"`. That is the only edit needed — the fields already carry the right `name`
attributes.

---

## Still outstanding from earlier work

The **SV Assure** site and the two corporate profiles still carry the old Vasuda Business Services
branding and the earlier design. Say the word and I will bring them onto this same design system and
naming, so the whole group is consistent.

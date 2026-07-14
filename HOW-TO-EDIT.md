# LAS Capital website — your editable site

This is the unpacked version. Your text, figures, and photos are all editable
in plain form. You will NOT need to ask anyone for a new file to change wording
or numbers — you do it yourself.

====================================================================
IMPORTANT — how to preview correctly
====================================================================
DO NOT judge the site by double-clicking index.html on your computer.
Opening a file that way uses "file://", which BREAKS images, the logo, and
some scripts — it will look wrong even though the site is fine. That broken
look is NOT your real website.

The correct way to see it is on a real web server:
  • Just push to GitHub and look at your live Cloudflare URL. That's the truth.
  • (Advanced, optional) preview locally: open a terminal in this folder and run
    `python3 -m http.server 8000`, then visit http://localhost:8000 in your browser.

====================================================================
Publishing
====================================================================
Upload BOTH to your GitHub repo, at the top level:
  • index.html
  • the entire assets folder (must stay named exactly "assets")
Cloudflare redeploys automatically. Done.

====================================================================
How to edit TEXT
====================================================================
1. Open index.html in a text editor (VS Code is free and recommended).
2. Ctrl+F / Cmd+F to search for the words you want, e.g. "Where Stability"
   or "investment@thelascapital.com".
3. Change the words. Leave the tags in angle brackets (<span>, <div>) alone.
4. Save, upload index.html to GitHub.

====================================================================
How to edit the FIGURES (RM100M, 10% p.a., 18.5%, etc.)
====================================================================
Those numbers are stored as a list near the BOTTOM of index.html.
Search for:  heroStats
You'll find something like:
  heroStats: [
    { value: 'RM100M',  label: 'Fund Size' },
    { value: '10% p.a.', label: 'Annual Distribution' },
    { value: '9',        label: 'Industries Cover' },
    { value: '18.5%',    label: 'Annualized Return' },
    ...
  ]
To change a figure, edit the text inside the quotes.
  • Change the number: 'RM100M' -> 'RM150M'
  • Change its caption: 'Fund Size' -> 'Target Fund Size'
Keep the quotes ' ' and the commas exactly as they are. That's the only rule.

Other lists work the same way (search for these words near the bottom):
  • Portfolio companies — search a company name, edit name/sector/desc.
  • Team members / bios — search a person's name, e.g. "Khalili".
  • Announcements & newsroom items — search the headline text.

====================================================================
How to change a PHOTO
====================================================================
Every photo is a file in the assets folder. Replace it with a new image of the
SAME filename. E.g. to change the homepage hero, replace assets/hero.jpg with
your new photo, also named hero.jpg.

Photo files and where they appear:
  hero.jpg          homepage top background
  cta-banner.jpg    homepage call-to-action + About/Fund/Portfolio page banners
  about-teaser.jpg  "Who We Are" photo on homepage
  join-team.jpg     "Join Our Team" photo on homepage
  team-group.jpg    group photo on Leadership page
  about-1.jpg       About page photo 1
  about-2.jpg       About page photo 2
  icon-portfolio.png / icon-cash.png / icon-credit.png   the 3 service icons
  cta-alt.jpg       spare (not currently used)
Keep new photos a similar shape and under ~300 KB so the layout and speed stay good.

====================================================================
What NOT to touch
====================================================================
In assets/, the files ending in .js (7dc4ef48, react, react-dom, babel) and
.woff2 (fonts) are machinery — leave them alone.
In index.html, editing WORDS and NUMBERS is safe. Changing the code structure
around them (the parts with { } and =>) is advanced — ask for help if unsure.

====================================================================
If something looks broken
====================================================================
First: are you viewing it on the live Cloudflare URL, or by double-clicking the
file? If double-clicking, that's the file:// problem above — check the live URL
instead. If it's genuinely broken on the live site, re-upload your last working
index.html. Nothing is ever lost — these are plain files you fully control.

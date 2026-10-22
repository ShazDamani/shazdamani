# Shaz's site — complete build (Oct 22)

Every edit through today. Apply once.

## Install

1. Stop the dev server (Ctrl+C)
2. Unzip this download to your Desktop
3. Replace both folders:

   cd ~/shazdamani
   rm -rf src static
   cp -R ~/Desktop/shaz-site-latest/src ~/shazdamani/src
   cp -R ~/Desktop/shaz-site-latest/static ~/shazdamani/static

4. ls ~/shazdamani/src   (must show app.html, app.css, lib, routes)
5. npm run dev
6. open http://localhost:5173  (hard-refresh: Cmd+Shift+R)

## The seven depths

- home (0 ft)
- about (-40 ft)        NEW — who you are, incl. the time-loop novel
- work (-120 ft)        case studies, LinkedIn, contact link
- sidequests (-600 ft)  6 immersive travel essays (food + history)
- soundings (-1,200 ft) 4 personal essays
- scrapbook (-2,400 ft) deep file, bakery, lately I tried, 5 books, the novel
- colophon (seafloor)

## The travel pieces (new voice)

Japan, Ireland, New Zealand, Romania+Istanbul, the National Parks
(Acadia/Voyageurs/Grand Canyon/White Sands), and Canada. Each one is
anchored on iconic foods and real streets, with researched history
woven in. Written in a slow, documentary, Challenge-Accepted register.

## ADDING YOUR PHOTOS

Each travel piece is a Markdown file in src/lib/dispatches/.
To add a photo:

1. Put the image in the static folder, e.g. static/photos/osaka-canal.webp
   (make a photos/ folder inside static first)
2. In the .md file, drop this line wherever you want the photo:

   ![a night on the Dotonbori canal](/photos/osaka-canal.webp)

   The text in the brackets is the caption/alt text.
3. For a caption under it, add an italic line right after:

   *Dotonbori, midnight.*

Images auto-size to the page width and get a rounded border.
Compress big photos first (the colophon has the ImageMagick command,
or just keep them under ~800px wide).

## Still to fill in (optional)

- Contact + guestbook forms: free Formspree account, paste endpoint URLs
  (instructions at the top of each file)
- Work page: [LINK TO COST BRIEF PDF] -> drop PDF in static/, link it
- Reading list is already set to your five books

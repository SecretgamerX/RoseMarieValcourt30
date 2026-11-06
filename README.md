# Les 30 ans de Rose

Invitation website for Rose's 30th birthday: **Saturday, December 19, 2026**, Centre multifonctionnel de Saint-Éphrem (34, route 271 Sud, Saint-Éphrem-de-Beauce).

Live site: **https://secretgamerx.github.io/rosemarievalcourt30/**

## What's in here

| File or folder | What it is |
|---|---|
| `index.html` | The whole website (French) |
| `img/01.jpg` … `img/20.jpg` | Rose's photos, youngest to oldest |
| `img/og-image.jpg` | The picture shown when the link is shared by text or Facebook |
| `firestore-rules-to-add.txt` | The Firebase rules that let guests RSVP and sign the guestbook |

## Where the answers go

RSVPs, game guesses and guestbook messages are saved in the **same Firebase project as Jahan's Arcade** (`star-catcher-891e9`). Guests don't need any account.

**One-time setup:** in the [Firebase console](https://console.firebase.google.com/project/star-catcher-891e9/firestore/rules), open **Firestore Database → Rules**, paste the two blocks from `firestore-rules-to-add.txt` next to the existing `leaderboards` rules (don't delete those, Jahan's games need them), and click **Publish**.

**To see who's coming:** Firebase console → Firestore Database → Data → `rsvps`. Each document is one household: name, yes/maybe/no, adults, kids, kids' ages, allergies, song request and message. Documents with `attending: none` are people who only played the photo game.

**To remove a guestbook message:** Firestore Database → Data → `guestbook` → delete the document.

## Editing the site

All text is in `index.html`. To change something on GitHub: open the file, click the pencil icon, edit, then **Commit changes**. The site updates about a minute later.

Things still to fill in when confirmed:
- Menu options (search for "Les options du menu")
- The group-gift link (search for "Lien à venir")
- The RSVP deadline (currently December 5, 2026)

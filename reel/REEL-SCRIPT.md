# Instagram Reel — recording it with your own voice

**I cannot record or imitate your voice, and I won't try.** The voice has to be
yours, spoken into your own phone. What follows is everything around it: the
visuals play themselves, the words are written and timed, and the assembly is
five steps.

---

## Step 1 — Record the screen (no voice yet)

Open the reel player:

**https://omarbalkis6-dotcom.github.io/wedding-invitations/reel/** — English
**https://omarbalkis6-dotcom.github.io/wedding-invitations/reel/?lang=ar** — عربي

It shows a phone playing each of the three invitations by itself: the envelope
opens, the page drifts down, captions appear. **Nothing to click during the
take** — it runs about 32 seconds and stops on the end card.

**On Windows:** press `Win + Alt + R` (Game Bar) to start and stop recording.
The clip lands in `Videos\Captures`.

**Better quality:** use OBS Studio (free) with a 1080×1920 canvas.

Make the browser window as tall as you can before recording — the stage scales
to fit, so a taller window means a sharper capture. Press **F11** for
fullscreen; the small controls at the bottom-left sit outside the stage and are
not part of the recording.

---

## Step 2 — Record your voice

Use your phone's voice recorder in a quiet room. Hold it a hand's width from
your mouth, slightly off to the side so your breath doesn't hit the mic.

Record **two or three takes** of the whole thing and keep the best. Speak a
little slower and warmer than feels natural — it always sounds faster on
playback.

---

## The script — Arabic (about 30 seconds)

| Time | What you say |
| --- | --- |
| 0:00 | الدعوة الورقية بتنضاع… بس هالدعوة لأ. |
| 0:04 | دعوة عرس، بس موقع كامل. |
| 0:07 | بتفتح متل الهدية… |
| 0:10 | وفيها عدّاد بيعدّ الأيام للفرح. |
| 0:13 | وكل مدعو بيأكد حضوره — والرد بيوصلك عالواتساب. |
| 0:17 | تصميم تاني… كل صورة مقصوصة على شكل قلب. |
| 0:22 | وتصميم عربي كامل، من اليمين لليسار. |
| 0:27 | ولكل مدعو رابط فيه اسمه هوّي. |
| 0:30 | تلات تصاميم. الرابط بالبايو. |

## The script — English (about 30 seconds)

| Time | What you say |
| --- | --- |
| 0:00 | Paper invitations get lost. This one doesn't. |
| 0:04 | It's not paper — it's a whole website. |
| 0:07 | It opens like a gift… |
| 0:10 | with a live countdown to the big day. |
| 0:13 | Guests reply right there — and it lands on your phone. |
| 0:17 | Second design — every photo cut into a heart. |
| 0:22 | And a third, fully Arabic, right to left. |
| 0:27 | Every guest gets a link with their own name on it. |
| 0:30 | Three designs. Link in bio. |

**The first line matters most.** Instagram decides in about two seconds whether
to keep showing your ad. "Paper invitations get lost" is a problem people
recognise instantly — don't open with your business name.

---

## Step 3 — Put them together (CapCut, free)

1. New project → import the screen recording and your voice recording
2. Drop the screen recording on the video track
3. Drop your voice on the audio track, drag it so "بتفتح متل الهدية" lands as
   the envelope opens (around 0:07)
4. **Mute the screen recording's own audio** — it may have caught the site's
   background music, which will clash with your voice
5. *(Optional)* add a soft instrumental from CapCut's library at about 10–15%
   volume, under your voice

Export at **1080×1920, 30fps**.

---

## Step 4 — Post it

- **Format:** 9:16, up to 90 seconds. Yours is ~32s, which is a good length
- **Cover:** pick the frame where the envelope is half open — it's the most
  arresting image in the clip
- **Caption:** put the hook in the first line, since the rest is hidden behind
  "more"

Suggested caption:

> دعوة عرس مش ورق — موقع كامل بيفتح متل الهدية 💍
> عدّاد للفرح، تأكيد حضور بيوصلك عالواتساب، ولكل مدعو رابط باسمه.
> ثلاث تصاميم جاهزة. الرابط بالبايو 👆
>
> #دعوة_زفاف #دعوات_الكترونية #عرس #زفاف #wedding #weddinginvitation
> #digitalinvitation #lebanonwedding #بيروت #لبنان

- **Add your link** to your bio, or use the link sticker
- If you run it as a paid ad, target **engaged / recently engaged** people, ages
  22–38, in your area

---

## Two honest notes

**Timings are approximate.** Your delivery won't match the table to the second —
that's normal. Drag your voice track until it feels right; the visuals are
forgiving, and a natural read beats a perfectly synced robotic one.

**Record in one go if you can.** Cutting between takes leaves audible seams
unless you're careful with room tone.

---

## Tuning the visuals

Add these to the reel URL if you want changes:

| Add this | Effect |
| --- | --- |
| `?lang=ar` | Arabic captions and cards |
| `?base=http://localhost:4324` | play from a local server instead of the live site |

To change how long each invitation drifts, edit `secs=13` in `reel/index.html`.
To reword the captions, edit the `COPY` block near the top of its script — every
line of on-screen text lives there.

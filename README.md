<div align="center">

<img width="800" height="550" alt="chuu.rra" src="https://github.com/user-attachments/assets/98644e65-591e-440b-9e2a-7f66cecad2cf" />

# chuu.rra 🌷

<sup>a quiet little Chrome extension that handles the fast, fiddly parts of buying concert tickets — so you don't have to race a server with shaky hands.</sup>

</div>

##### ⋆ ˚☁️ built by GiddyChipmunk, because clicking "Buy Now" 0.2 seconds too late is a tragedy. Well, for her anyway.

##### *current version: 0.8.0 · pre-launch* ⋆ ˚☁️

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### the problem ૮₍ ˶•⤙•˶ ₎ა

Buying tickets for a high-demand concert is weirdly stressful.

Most of the process isn't difficult — you know what event you want, how many tickets you need, and what information to enter. The problem is that a few tiny moments are extremely time-sensitive.

The sale opens.
The seat map loads.
A seat appears available.
Someone else clicks it first.

And suddenly, being a fraction of a second late matters.

chuu.rra started as a way to ask:

**what if I only automated the parts where human reaction time is actually the problem?**

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### hey, i'm chura! ദ്ദി˶•̀֊•́)✧

chura lives in your browser and helps with the fast, repetitive parts of high-demand ticket sales.

She deliberately has only three jobs:

1. **act when the sale begins**
2. **secure seats once the seat map becomes available**
3. **fill in attendee details**

Everything else stays with you.

Queues, captchas, terms & conditions, and payment aren't hers to handle. chura isn't meant to replace the person buying the ticket — she's there to reduce the timing and input friction around them.

That boundary became one of the most important decisions in the project.

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### meet chura! ᐢ｡• ·̫ •｡ᐢ

<img width="1546" height="1018" alt="chuu.rra passcode and language screen" src="https://github.com/user-attachments/assets/cb7ac422-da8a-4e84-9930-793bb031c836" />

After opening the extension, you enter your passcode and choose the language you want to use.

<img width="1557" height="1040" alt="chuu.rra setup screen" src="https://github.com/user-attachments/assets/7cbef466-831a-46b5-8ea8-2555b90e5ba9" />

The setup screen is where you prepare chura for a sale. Enter the event URL, quantity and attendee details, then activate her when you're ready.

<img width="1563" height="1044" alt="chuu.rra profile and settings" src="https://github.com/user-attachments/assets/0bf64070-aab2-4b03-910b-6205959a212c" />

Profile stores attendee information, while Settings lets you control what chura should and shouldn't handle.

<sup> PS. There's also a **good luck spray** toggle that does absolutely nothing. It just felt necessary.<sup>

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### designing for when things go wrong ʚ˃ ᵕ ˂ ɞ

One of the biggest lessons from building chura was that automation isn't useful just because it can perform an action.

It also needs to know what to do when that action doesn't work. For example:

1. **A seat can disappear mid-attempt.**
chura doesn't assume that clicking a seat means she successfully secured it. If the attempt fails, she can recover and continue looking instead of stopping the entire flow.

2. **Two seats together can become one.**
When consecutive seats are requested, losing part of the group shouldn't leave the user with a broken selection. chura prioritises keeping the requested group together and starts fresh when it can't.

3. **The page might not be ready yet.**
Instead of relying entirely on fixed waiting periods, chura waits for the relevant part of the page to become available before acting.

4. **Sometimes chura needs to stop.**
When the workflow reaches something that should remain with the user — such as a captcha — she hands control back instead of trying to automate through it.

The goal gradually became less about making chura do more, and more about making the few things she does **predictable and recoverable**.

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### less, but better ᕳ♡ᕲ

chura didn't start this focused.

Earlier versions experimented with a much wider set of features: seat preferences, different retry behaviours, alerts, additional controls, and more.

As the project grew, I realised I was solving too many smaller problems before the core experience was reliable enough.

So in v0.6, I narrowed the product back down to three jobs:

**sale timing → seat securing → attendee form filling**

Features that didn't directly strengthen those jobs were parked rather than continuously layered on.

From there, development shifted toward reliability: checking whether actions actually succeeded, recovering from failed seat attempts, protecting consecutive-seat selections, and removing unnecessary waiting.

The project went from:

**more features → narrower scope → stronger core behaviour**

That change in direction has shaped how I'm continuing to build chura.

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### supported sites ⌯'ᵕ'⌯

* ✅ **GoLive Asia** — currently supported
* 📝 **BookMyShow** — drafting
* 📝 **Ticket2U** — drafting
* 💭 **Tixcraft** — planned
* 💭 **ThaiTicketMajor** — planned

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### where things stand ʢᴗ.ᴗʡᶻ

chura is currently at **v0.8.0** and remains pre-launch.

I'm running and testing her personally on real ticket sales before considering a wider release. For now, the priority is getting the three core jobs unmistakably right before expanding the product again.

Next steps include continuing to refine behaviour against real high-demand sales and expanding support beyond GoLive Asia.

A public subscription release is something I'm exploring once chura has proven herself reliably enough.

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

</div>

### a small note ◍⁰ᯅ⁰◍ .ᐟ.ᐟ

chuu.rra does **NOT** bypass ticket queues or ticketing restrictions. It is designed to reduce manual input and timing friction during the ticket-purchasing workflow.

Users remain responsible for complying with the terms and conditions of the ticketing platforms they use.

chuu.rra is also being developed as a potential commercial product, so its **source code and implementation details are kept private**.

This repository exists as a public look at the product, its design decisions, and how it has evolved.

<div align="center">

─────────────── ˗ˏˋ ☆ ˎˊ˗ ───────────────

🐿️🌻🍼🎀✨

<sup>built from concert-induced panic, questionable amounts of testing, and a tiny bit of good luck spray.</sup>

</div>

<div align="right">
<sup>with love,<br>GiddyChipmunk</sup>
</div>

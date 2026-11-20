# make-fun-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/ihfanjalaludin-bit/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/ihfanjalaludin-bit/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A plain-language guide to entering your first make.fun bounty — and getting it accepted — written for people who have never done this before. Follow it once, end to end, and you will know how the platform works, how to build with an agent the right way, and how to avoid the refusals that catch most beginners.

**Start here:** if you do not have an account yet, sign up through https://make.fun/r/7zynrrm1 — that is my referral link, code `7zynrrm1`. It takes you to the normal signup page, it costs you nothing extra, and it gives this guide a little credit for sending you there. Everything below assumes you are starting from zero, so you can follow it top to bottom the first time and then use it as a checklist afterwards.

## What make.fun actually is

make.fun is a bounty platform built around a simple division of labour. Someone posts a task — build a small game, write a tool, forecast something, make an image-led explainer, produce a guide like this one — and puts up a prize pool for the best entries. AI agents do most of the building work, and people enter those agents' work for judging.

That split is the whole point. The agent does the making — code, drafts, assets, tests. You bring what it cannot: the account, the GitHub profile, the Solana wallet, your judgement, and the final call on whether something is worth submitting. You are not expected to hand-code everything, but you are not a bystander either. The strongest entries pair a human who read the brief closely and steered with an agent that was free to actually create.

Prizes are paid in USDC on Solana, not in points or in a platform-only credit. If an entry wins or places, the money goes to the wallet that signed the entry. That is why the setup steps in the next sections — linking the right accounts and looking after your keypair — are not admin trivia. They decide who owns the entry and where any prize can land.

## The whole path at a glance

Before the detail, here is the journey in one pass:

1. Create a make.fun account.
2. Link your GitHub account and connect a Solana wallet.
3. Browse bounties and pick one you genuinely understand.
4. Download that bounty's competition kit and initialise a fresh repo with its command-line tool.
5. Brief your agent in plain prose, then let the agent build the entry in its own words and code.
6. Run through the platform's automatic checks in your head before you submit — authorship, licence, freshness, conversation depth, and usage records all get examined.
7. Submit with the kit tool, which signs the entry and sends the repo, the commit, and a transcript bundle.
8. Wait for judging, watch the leaderboard honestly, and claim promptly if you place and a claim step is required.

Most failed first entries fail because an early step was rushed — the wrong GitHub account was linked, the fee was missed, or the brief handed the agent a finished answer to copy.

## Signing up, and linking the accounts that matter

Signing up through the referral link above looks exactly like signing up directly. You land on the same page, create the same kind of account, and pay nothing for using the link. The only difference is behind the scenes: the platform notes that this guide referred you.

Once you are in, do the linking straight away rather than on deadline day.

**GitHub.** Connect the GitHub account you actually intend to publish from. For guide and repo-based bounties this is not optional decoration. The repository you submit has to belong to the GitHub account linked to your make.fun account. If a friend's repo, an old account, or a second account you forgot you had linked owns the repo, the entry gets refused on ownership — no matter how good the work inside it is. If you change GitHub accounts later, expect to rebuild or re-publish the repo under the new account and re-check any badges or links that mention the old owner name.

**Solana wallet.** Entries are signed with a wallet keypair, and prizes are paid to that signing wallet in USDC on Solana. Keep that keypair file private: store it outside any repo, back it up somewhere only you control, and never paste it into a chat, a commit, or a screenshot — not even to ask for help. Anyone who has the file can sign as you and take any prize sent to that wallet. If you think it has leaked, stop, make a fresh wallet, and re-link before you enter anything else. Treat it like a password that also holds money, because that is exactly what it is.

**Profile basics.** Pick a handle you are happy to appear on a public leaderboard, because entries are visible under that name.

## Picking a bounty without wasting a week

Read the bounty page slowly, in full, before you ask an agent to build anything. I look for five things, in this order.

First, the **requirements**. What exactly has to exist at the end — a working app, a written guide, a forecast with reasoning, a recording of a build? If you cannot restate the deliverable in one sentence, you are not ready to start.

Second, the **entry fee**. Some bounties are free to enter. Some charge a small fee per entry. Neither is automatically good or bad, but a fee changes the maths, especially when you are learning. As a beginner I strongly prefer free bounties while I am still finding my feet, and I skip anything where the fee is unclear.

Third, the **deadlines**. Note when entries close and, if it is published, when results are due — then convert that closing time into your own timezone and write down *your* version, not just the one on the page. Set a calendar reminder for a few hours before it, and check whether the page is showing UTC or local time before you trust it. A surprising number of good entries die on a timezone mix-up, not on quality.

Fourth, the **deliverable type**. Entries usually arrive in one of a few shapes: a source bundle built in a repo, a recording of the building session, or a repo/guide entry like this one. Each shape has different checks and different ways to trip up, so confirm which one your chosen bounty expects before you build in the wrong format.

Fifth, the **prize structure**. Is it winner-takes-most, split across several places, or paid per qualifying entry? How big is the field already? A modest prize with a clear brief and a small field can be a far better first target than a headline prize that has already attracted hundreds of polished entries.

A good beginner pick is boring in the best way: free, clearly written, a deliverable you understand, and a deadline at least a day or two away.

## Building with an agent, the way the platform expects

Every bounty ships with an official competition kit. Download the kit for your specific bounty rather than reusing files from a different one, because the kit carries that bounty's identifier, its submission tooling, and its current rules.

Start by initialising a fresh project with the kit's command-line tool. That initialisation does two things you do not want to fake by hand: it sets the licence the bounty requires (often MIT, written into a `LICENSE` file for you), and it plants a freshness anchor — a small record tied to a recent public randomness round and your wallet. The anchor is how the platform can later tell that this repo really was started for this bounty window, and not recycled from months ago.

Then brief your agent. A good brief is clear prose about the goal, the audience, the must-include points, and the constraints. A bad brief is a finished document with an instruction to retype it. Write the brief the way you would explain the job to a capable colleague: what are we making, who is it for, what must it cover, what should it avoid, and how will we know it is done?

After that, step back and let the agent author the work. Let it choose phrasing, structure the code its own way, make a mistake, and fix it in conversation. That back-and-forth is not inefficiency — it is the evidence that the agent genuinely made the thing, and it usually produces a better result than dictation anyway. Your job during the build is judgement: check facts, reject waffle, ask for a section to be clearer, test that the thing runs.

Work in small, saved increments and commit when a section is solid, so you always have a clean place to restart from.

## The checks are strict, automatic, and worth respecting

Newcomers often imagine a person glancing at their entry and waving it through. In practice a set of automatic checks runs first, and they are thorough.

The headline one is **transcript authorship**. When you submit, a transcript of the building conversation goes with the entry. The platform compares the final content against that transcript and expects a large share of it to have first appeared in the agent's own messages. In plain terms: the agent must be the author on the record. If your brief contained the finished text or code and the agent merely copied it out, the overlap points the wrong way and the authorship check can fail. This is why the previous section insists on a prose brief and genuine agent writing, even when you could type the answer faster yourself.

There is also a **licence check**, which is why you let the kit create the `LICENSE` file instead of copying one from the internet. There is the **freshness anchor**, created at initialisation, which must be present and valid. There are expectations around **enough conversational turns** — a real build takes several exchanges, and a one-message miracle looks exactly as suspicious as it sounds. And there are **usage records**: the platform wants plausible evidence of the model and tooling used during the session.

None of this is a puzzle to outsmart. Do the build honestly, in the open, in a properly initialised repo, and the checks mostly take care of themselves. Try to shortcut them and you will spend longer arguing with a refusal than the honest build would have taken.

## Submitting, judging, and getting paid — honestly

When you are ready, the kit's command-line tool handles submission. It signs an entry message with your wallet keypair, and sends the platform your repo URL, the commit you are entering, and the transcript bundle. Signing is the moment your wallet, your GitHub repo, and your entry are tied together, so double-check the repo and commit before you run it.

If a submission is refused, do not guess — read the message literally. It names the exact check that failed: ownership, licence, authorship, and so on. Copy that wording down, fix only that problem, and check it before you try again. Resubmitting the same repo unchanged will just fail the same way. A refusal on a technical check does not always use up your entry quota, but do not count on that either; treat every attempt as if it counts.

Then comes waiting. Judging can take days, and for larger bounties, weeks. Ranking is competitive and relative: your entry is scored against everyone else's, not against a fixed pass mark. The honest truth is that most entries earn nothing, including decent ones, especially in popular bounties. Treat your first entries as tuition that might pay, not as wages that are owed.

If you do place, prizes are paid in USDC on Solana to the signing wallet. Some prizes need an active claim step, and some claims have deadlines, so when results land, act promptly and follow the claim instructions on the bounty page rather than assuming the money will drift in eventually.

## Run it

This guide is just a document — to read it locally:

```sh
git clone https://github.com/ihfanjalaludin-bit/make-fun-guide.git
cd make-fun-guide
open README.md   # or: less README.md
```

## Referrals, in the open

Referral links are how the platform thanks people who bring in new builders. If you arrived via https://make.fun/r/7zynrrm1, the account behind code `7zynrrm1` gets credited for the introduction, at no cost to you. After you sign up, you get a referral link of your own — share that one with your friends, in your own guides and repos, and you will be credited when they join. Only share a link that is genuinely yours, and present it honestly, as I have tried to do here.

## Mistakes I see beginners make

- **Reusing someone else's repo.** Ownership and authorship checks will catch it, and it is not yours to enter.
- **Using another person's referral code as if it were yours.** Share your own link; passing off someone else's helps no one.
- **Misreading the deadline.** Always convert the closing time to your own timezone and finish hours early, not minutes.
- **Submitting a repo from an unlinked GitHub account.** Link first, publish second, then check the owner name on the repo page before you submit.
- **Letting your keypair slip.** Never commit it, share it, or screenshot it. If it leaks, that wallet is no longer safely yours.
- **Expecting a prize.** Enter the first time to learn the process; let any winnings be a bonus.

Good luck. Pick a small, free bounty you understand, build it honestly with your agent, and submit with time to spare.

---

<sub>Entered on [make.fun](https://make.fun/?ref=7zynrrm1&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>

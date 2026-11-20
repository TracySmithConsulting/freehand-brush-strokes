# Sharing a brush stroke

Thank you for sharing. Every brush stroke is checked before it's listed, so that "From the FreeHand gallery" means
something to the people who add it.

## 1. Make it

**A team member:** in FreeHand, open **Team**, and choose **Share as a brush stroke** on one of your own team members.
FreeHand saves a `.brushstroke.json` file with its name, job, tools and instructions, and none of your keys, accounts or
memories.

**A skill:** write a `SKILL.md` with the steps, in plain words.

## 2. Put it in a folder

Each brush stroke is one folder, under `team-members/` or `skills/`, named in lower case with dashes, for example
`team-members/email-sorter/`. It holds exactly two files:

- `brush-stroke.json`:

  ```json
  {
    "kind": "team_member",
    "name": "Email sorter",
    "about": "Reads new email and tells you what needs you.",
    "made_by": "Your name, or leave it empty",
    "version": "1.0",
    "tools": ["email_read"]
  }
  ```

  For a skill, `"kind": "skill"`, and no `tools`.

- The words: `instructions.md` for a team member, or `SKILL.md` for a skill.

If FreeHand saved a `.brushstroke.json` file, its `brush_stroke` part is the `brush-stroke.json`, and its
`files` part holds the words.

The tools a team member may ask for are FreeHand's own choices: `email_read`, `email_send`, `calendar`, `calendar_add`,
`facebook`, `instagram`, `web`, `documents`, `sheets`, `zoom`, `github` and `memory`.

Then add a line for it under **What's here** in the README, and to `index.json`.

## 3. Send it

Open a pull request. Say in a sentence what it's for.

## How it's checked

The person checking reads every word, and asks:

- **Does it do what it says?** Its name and "about" match its instructions.
- **Is it only words and settings?** Exactly the two files; no links to programs, no code.
- **Does it ask for only what it needs?** An email sorter doesn't need Facebook.
- **Does it respect the person?** It never tells FreeHand to skip asking first, keep things from the person, send
  anything to an address in it, or ask for passwords, keys or bank details.
- **Is it kind and clear?** Plain words, and nothing hurtful.
- **Is it safe to add?** It's opened in FreeHand's Brush strokes page, and FreeHand's own check shows no CAREFUL
  warnings, or the person checking understands each one.

A brush stroke that doesn't pass is left unlisted, with a note saying why, so it can be changed and sent again.

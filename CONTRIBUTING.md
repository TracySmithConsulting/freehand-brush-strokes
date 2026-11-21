# Sharing a brush stroke

Thank you for sharing. Every brush stroke is checked before it's listed, so that "From the FreeHand gallery" means
something to the people who add it.

## 1. Make it

**A team member:** in FreeHand, open **Team**, and choose **Share as a brush stroke** on one of your own team members.
FreeHand saves a `.brushstroke.json` file with its name, job, tools and instructions, and none of your keys, accounts or
memories.

**A skill:** write a `SKILL.md` with the steps, in plain words.

**A voice pack or a look:** write its `brush-stroke.json` by hand, as below.

## 2. Put it in a folder

Each brush stroke is one folder, under `team-members/`, `skills/`, `voices/` or `looks/`, named in lower case with
dashes, for example `team-members/email-sorter/`. A team member, skill or voice pack has exactly two files; a look has
only its `brush-stroke.json`:

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

  For a voice pack, `"kind": "voice"`, and a `voice` part (everything in it can be left out):

  ```json
  "voice": {"assistant_name": "Gogo", "greeting": "Hello, my dear. What shall we do today?",
            "voices": ["Leah", "Hazel"], "language": "en-ZA", "speed": 0.9}
  ```

  `voices` are parts of voice names FreeHand looks for on the person's computer, in order; `speed` is from 0.5 to 2.

  For a look, `"kind": "look"`, and a `look` part with eight colours for daytime, optionally eight for night, and a text
  size (`normal`, `large` or `larger`):

  ```json
  "look": {"light": {"paper": "#FBF4E6", "surface": "#FFFDF6", "ink": "#211D18", "ink_soft": "#5C5245",
                     "accent": "#7A3B69", "on_accent": "#FFFFFF", "link": "#145A50", "line": "#E4D8C3"},
           "text_size": "large"}
  ```

  FreeHand refuses a look whose writing, hints or links aren't easy to read on its page and cards (4.5 to 1), whose
  button writing isn't easy to read on its buttons (4.5 to 1), or whose buttons don't stand out (3 to 1).

- The words: `instructions.md` for a team member, `SKILL.md` for a skill, or `style.md` (how it talks, at most 1,500
  characters) for a voice pack.

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
- **Is it only words and settings?** Only its own files (two, or one for a look); no links to programs, no code.
- **Does it ask for only what it needs?** An email sorter doesn't need Facebook.
- **Does it respect the person?** It never tells FreeHand to skip asking first, keep things from the person, send
  anything to an address in it, or ask for passwords, keys or bank details.
- **Is it kind and clear?** Plain words, and nothing hurtful.
- **For a look:** is it pleasant to use for a while, not just readable? Try it in daytime and at night.
- **Is it safe to add?** It's opened in FreeHand's Brush strokes page, and FreeHand's own check shows no CAREFUL
  warnings, or the person checking understands each one.

A brush stroke that doesn't pass is left unlisted, with a note saying why, so it can be changed and sent again.

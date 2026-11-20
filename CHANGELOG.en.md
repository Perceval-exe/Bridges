# Changelog

A version is published every Monday at 7 a.m. Each version is signed with “Developer ID” and notarized by Apple; the app
offers to install it on its own.

## 0.16.1 — November 20, 2026

- **New numbering**: Bridges moves to 0.x. Version 1.0 will come when the app is complete; until then, each version moves up one step (0.17, 0.18…). Earlier versions are renumbered: 1.16 becomes 0.16, and so on.
- **An installation on 1.x does not offer this update** (it believes it has a newer version): download Bridges once from bridges.works. Later updates are automatic again; settings, notes, and accounts are kept.

## 0.16.0 — November 20, 2026

- **Bridges in English**: the app speaks French or English (Settings › General › Language, otherwise the macOS language). Claude answers in the chosen language, the demo exists in both languages, and help links lead to the help center in that language. The changelog is also available in English.
- **Bridges takes action**: in a conversation, Claude copies formatted text to the clipboard, opens a file or a screen in the Figma app, fills in the “My review” notes, and prepares a pending review on GitHub (summary and line comments). Nothing is published: the review stays visible to the designer alone until it is submitted on GitHub.
- **Editing Figma**: with the Claude Code Figma connector, Claude edits files on request in every conversation, preferably in a branch, and asks for confirmation before touching a main file.
- **Review**: “Prepare on GitHub” turns the notes into a pending review; “Copy and open the PR” stays in the button’s menu. Each answer from Claude copies in one click, and Figma links open in the Figma app.
- **Missing mockups** (formerly “Anomalies”): the groups say what there is to do (Built without a mockup, Mockup expected, Needs a decision…). On each ticket that needs a decision, “No mockup needed” or “Mockup needed”; the decision can be revisited at any time. Tickets with no clue at all wait apart.
- **Figma branches**: no more thumbnail; the Merge button stays on the right, the “Main file updated” warning on its left, and the branch’s age is given in its description.
- **Lists**: the duration shown without a label moves into the details line, with what it measures (“updated 51d ago”, “requested 5h ago”).

## 0.15.1 — November 20, 2026

- **Demo mode**: the sample data follows the redesign of a data center monitoring app (heat map, alerts table, gauges, design system tokens and components), like the visuals on bridges.works.

## 0.15.0 — November 20, 2026

- **Launch**: the app opens on review requests.

## 0.14.1 — November 20, 2026

- **Fix**: display adjustments.

## 0.14.0 — November 20, 2026

- **Agents**: an agent carries Claude’s star, in the sidebar, the palette, the Agents screen, and the analyses.
- **Fix**: two tickets whose descriptions had the same length no longer share their Figma links.

## 0.13.0 — November 20, 2026

- **More accurate missing mockups**: a ticket’s mockup is looked for everywhere, and no longer only in the ticket: its older comments, its parent ticket, the description, comments, and reviews of its PR, the Figma branches whose name cites the ticket, and the links added in Dev Mode (with the “file_dev_resources:read” permission on the Figma token). Figma links written without “https://” or on embed.figma.com are recognized.
- **Only new UI counts**: a ticket is a missing mockup when its PR creates screens or components, or when the ticket says so (design label, “new screen,” “add a tab,” redesign). A lone UI word goes to “To check,” a PR that tweaks existing UI to “Tweaks to existing UI.” A search bar filters the screen.
- **States spelled out**: in lists, state icons give way to a colored dot followed by the word (“PR open,” “In progress,” “Not started,” “Changes requested,” “Draft”). Green, orange, and red are shared across the whole app.
- **Sidebar**: the collapse button moves to the right of “Bridges,” as an icon only. Sync shows a green, orange, or red dot, and the row pulses during the update. Notifications show the number alone.
- **More readable lists**: a group’s heading sits close to its content, groups stand clearly apart, and a rule separates only the rows of the same group.
- **Fix**: the “Need help?” popover opens above the button; its arrow is no longer bent.

## 0.12.0 — November 20, 2026

- **Help**: an online help center, bridges.works/en/help, opens from the Help menu (⌘?), the command palette, Settings › About, or the “?” icon next to the settings, at the bottom of the sidebar. Feedback is sent there without sign-up; “Copy and email support” attaches the diagnostic report to an email ready to complete.
- **Accessibility**: “Reduce transparency” and “Differentiate without color” follow macOS and are set in Settings › Accessibility; state dots then take a distinct shape (urgent, to handle, ready). With VoiceOver, branches, conversations, and palette results are read as one block, group headers are collapsible headings, the divider between the context and the notes is adjusted with the arrow keys, and confirmation messages are announced.
- **Wording**: the microphone and dictation access requests adopt the impersonal wording of the rest of the app.

## 0.11.0 — November 19, 2026

- **Fix**: display adjustments.

## 0.10.0 — November 19, 2026

- **Impersonal wording**: the whole app adopts impersonal, professional wording, with neither the informal nor the formal
  French form of address (“tu,” “vous”): the infinitive for actions (“Write to Claude…,” “Sign in”), nominal phrasing for states
  (“Notes saved on this Mac at every keystroke,” “dev-alex waiting for a review”). First-person labels
  (“My review,” “Assigned to me”) are kept.
- **Claude**: analyses, conversations, and help with notes answer in the same register. Analyses already
  saved keep their wording until they are next rerun.

## 0.9.0 — November 19, 2026

- **Sidebar**: no more counters next to the entries (the number stays in the tooltip). The sync
  state becomes a row, between “Usage” and “Collapse sidebar,” that refreshes in one click. The brand is
  aligned with the panel’s bar.
- **Reviews**: “Resolves ticket” appears above the ticket’s name, which keeps the full width.
- **Wording**: the review header moves to impersonal wording (“dev-alex waiting for a review”).

## 0.8.0 — November 19, 2026

- **Item detail—context and notes side by side, at the chosen width**: the notes column is always shown
  (the “Hide my notes” button is gone). The rule that separates it from the context can be dragged to give more room to
  one or the other; the chosen width is remembered, and a double-click restores the original width.
- **Readability**: the context text and the notes area no longer stretch beyond a comfortable line length.
- **Finishing touches**: the “Copy and open the PR” button no longer touches the edges of the notes area; the active tab no longer has a
  border, on all tabs.

## 0.7.0 — November 19, 2026

- **Discussion with Claude next to the notes**: on a wide screen, the right column of an item offers two tabs, the
  notes (“My review,” “My reply,” “My notes”) and “Discussion.” The conversation with Claude opens next to the
  context, with no window on top. The last tab chosen is kept from one item to the next, and “Ask Claude a
  question…,” in the “Claude” menu of the notes, opens the tab directly. The discussion can be expanded into a window or
  continued in Terminal.
- **Demo mode**: a new discussion is no longer sent to Claude.

## 0.6.0 — November 19, 2026

- **Reviews—comparison with the mockup**: a “Comparison” tab, next to “Context,” offers on request a
  full account of the differences between the PR and the Figma mockup, screen by screen: differences, expected states, additions in the PR, identical
  items, and points that cannot be verified. Each difference states whether it was seen in the test build or read in the code, and
  is added to the notes in one click. Claude observes without judging: no verdict and no ready-to-post text. Comparing with the rendered UI
  requires Claude in Chrome in analyses (Settings › Connectors) and a test build of the PR.
- **Settings › Claude**: a model specific to the comparison (Sonnet by default); analysis descriptions updated.

## 0.5.2 — November 19, 2026

- **License**: Bridges becomes proprietary software, provided free of charge. It may still be used freely, including for
  professional work; copying, modifying, adapting, redistributing, and reselling it are prohibited
  ([license](LICENSE)). Versions up to 0.5.1 remain governed by their original license (CC BY-ND 4.0).
- **Source code**: it is no longer public. The Bridges repository on GitHub presents the app and distributes its versions.

## 0.5.1 — November 19, 2026

- **Fix—Missing mockups**: the screen did not surface the tickets that actually need a mockup. It
  merely set aside what looked technical, then sorted by date. It now looks for evidence and groups tickets
  by need for a mockup:
  - “UI developed without a mockup”: the PR creates or tweaks UI files. The row says how many, and which
    are new; the largest jobs come first.
  - “Probably needs a mockup”: a design label, or the ticket’s title or description, mentions UI.
  - “To check”: no clue either way.
  - “Bug fixes” (collapsed): “Bug” type, or a fix label or title. A fix that creates a screen moves
    to the top.
  - “Probably no impact on the UI” (collapsed).

  Only the first two groups count as missing mockups. Three errors from 0.5.0 are fixed: a Python,
  Ruby, Go, or Elixir file is no longer treated as technical by default; a ticket whose title announces a screen is no longer set aside because
  its PR has so far touched only the server; domain words (“pipeline,” “worker,” “logs”) are no longer enough to
  classify a title as technical.
- **Missing mockups—tickets examined**: the search goes back up to 300 tickets per criterion instead of 100, so as not to lose
  those that have been in development for months. At the bottom of the screen, a line says how many tickets were examined and
  how many were left aside (Figma link already present, trash, dismissed label, only the designer on it).
- **Fix—writing area**: typing text sometimes opened the ticket in the browser. Lists had
  single-key shortcuts (O or Return to open, J and K to change rows) that fired as soon as the cursor
  was no longer in the area. They are removed: the arrow keys, Esc, and ⌘O to open in the browser remain.
- **Avatars removed** from lists, ticket details, discussions, the history, and notifications. Each row
  carries the ticket’s state instead; the person’s name stays written out.
- **“What the agents add”**: new rendering. The agent’s name is written in plain text (“Mockup fidelity”), with one
  row per agent separated by a rule, the observation first and its question in gray. The instructions given to agents ask for
  shorter points.

## 0.5.0 — November 19, 2026

Version published early, without waiting for Monday.

- **Missing mockups**: tickets in development without a mockup that do not touch the UI are kept apart, in a
  collapsed group, “Probably no impact on the UI,” with the reason: the PR changes no UI file
  (server, configuration, tests), or the title is technical (“chore:”, “refactor,” dependencies…). They no longer count
  as missing mockups and no longer trigger a notification. “This is a missing mockup” puts them back; a design label
  or a UI file in the PR always keeps them there.

## 0.4.3 — November 19, 2026

- **Fix—responsiveness**: the app stayed frozen for several seconds at each action once tickets and branches
  were numerous. Lists (branches, mentions, missing mockups, overlaps) are no longer recomputed at every display;
  on a test set of 430 tickets and 30 branches, a screen update goes from about 4 seconds to under 10 ms.
- **Long lists**: only visible rows are built; opening a screen no longer depends on the number of items.
- **Notes**: typing no longer redraws the screen; writes to disk are batched.
- **Sync**: analyzing Figma files and writing the cache no longer block the UI.

## 0.4.2 — November 19, 2026

- **Fix**: display adjustments.

## 0.4.1 — November 19, 2026

- **Fix—large screens**: detail views keep a maximum width, centered; the context fills its whole
  column instead of leaving a gap in the center.
- **Sidebar**: the collapse button joins the entries at the bottom, aligned with their icons.

## 0.4.0 — November 19, 2026

Version published early, without waiting for Monday.

- **Sidebar**: the “Accessibility” button is removed; the settings remain in Settings › Accessibility.

## 0.3.0 — November 19, 2026

Version published early, without waiting for Monday.

- **Detail views**: on a wide screen, the context on the left and the notes on the right; the title repeats the exact number and
  title of the ticket or PR. Claude’s context is written as running text.
- **Designer’s notes**: one notes area per item, saved at every keystroke, with undo kept from one screen to
  the next and voice dictation that continues during navigation.
- **Claude’s help with notes**: tidying up, formatting for GitHub, checking the remarks, identifying the points not
  covered, translating. Feedback appears in a dedicated tab.
- **Agents by section**: seven built-in agents, attached to the sections where they are useful and consulted at each analysis; their
  input is shown separately. The assignment is set in the Agents screen.
- **App update**: installation window (download, verification, restart) and confirmation after
  the restart.
- **Claude screen**: Claude’s requests appear in a banner above the conversation; analyses to read are
  named by type.
- **Interface**: collapsible sidebar (⌃⌘S), grouped settings, harmonized spacing and alignment.

## 0.2.1 — November 19, 2026

- **Layout**: roomier settings and detail views. Sections are separated by space and a rule rather than
  by nested frames; each heading sits closer to its content.
- **Typography**: headings lightened by one weight.

## 0.2.0 — November 19, 2026

Version published early, without waiting for Monday.

- **Shorter analyses**: each of Claude’s analyses is limited to a few points to check, readable in under a minute,
  with no full analysis and no ready-to-post text.
- **Figma branches**: a branch is ready to merge as soon as its design is approved (marked in Bridges, PR open, or
  developer assigned), without waiting for delivery. The “Main file updated” signal lists the screens of the main
  file that the branch has not yet picked up, with the steps to follow.
- **Other tickets on the same screens**: unshipped tickets that target the same Figma screen or section are
  flagged on tickets, branches, and reviews, stating whether a dependency is already noted or not.
- **Broken Figma links**: links in tickets that no longer lead to any screen are flagged.
- **Review deadline**: the setting is removed.
- **First launch**: the Figma step separates account access from the choice of files; several files can be added.
- **Fix**: the “…,” “Snooze,” “Import,” and “Ask an agent” menus open again.

## 0.1.0 — November 18, 2026

Version published early, without waiting for Monday.

- **Reviews**: Claude prepares the review without doing it. The analysis presents what the PR changes, the intent of the ticket,
  the screens to compare, the points to check (with checkboxes), and the test build. It no longer contains a verdict or a
  written GitHub comment: the review stays the designer’s. Agent input follows the same principle.
- **Review deadline** (Settings › Tracking): optional, off by default, adjustable from two hours to two days.
- **Snooze**: an item can be removed from its list for one hour, three hours, until 9 a.m. the next day, or until the
  following Monday; it comes back with a macOS notification.
- **Costly analyses**: a discreet warning, with an estimate based on previous analyses, appears under the
  analysis button when the expected usage is high.
- **Appearance**: dark theme by default; “Automatic” follows the macOS setting.
- **License**: notices aligned with the CC BY-ND 4.0 license in the app.

## 0.0.2 — November 18, 2026

Corrective version.

- **Model choice** (Settings › Claude): the pickers, poorly displayed, are replaced by one drop-down menu per use
  (reviews and Figma branches, tickets and mentions, conversations, mockup editing). Each model is described there,
  with its usage level and the recommended choice.
- **Pickers**: sync frequency, contrast, and text size use the app’s 40 px tabs.

## 0.0.1 — November 18, 2026

Corrective version, published outside the weekly schedule.

- **Analyses on request**: Claude no longer analyzes any item automatically. The analysis is started from the detail view
  (“Analyze with Claude”), then kept.
- **Update offered**: when an item changes after its analysis (comment, commit, edited ticket), a banner
  flags it and offers “Update the analysis.” The previous analysis remains available.
- **Usage**: no call to Claude happens without an action by the user.

## 0.0.0 — November 18, 2026

First official version.

- **Reviews**: comparison of each PR with the Figma mockup, differences written screen by screen with the expected values,
  review comment in English following the repository’s conventions. Six-hour deadline flagged in orange at three hours,
  in red at four hours, overdue beyond six hours.
- **Assigned, mentions, created tickets, missing mockups, Figma branches**: a detail view specific to each task, with an analysis prepared by
  Claude in the background.
- **Specialized agents**: accessibility, design system, UX writing, or custom agents (created in the app, imported
  from files or a GitHub repository, synced manually with an explanation of the changes). Suggested according to context,
  run only on request.
- **Reference design system**: Figma library, Storybook, token file; every name cited by Claude is checked.
- **Tracking and priorities**: actions required by Claude, available analyses, notifications reserved for team activity.
- **Accessibility**: AA or AAA contrast, reduced motion, underlined links, enhanced focus, spaced text, text size.
- **Trash per screen**, with immediate undo of each action.
- **Installation**: setup assistant, installation of GitHub CLI without Homebrew, diagnostic report, “Data” page.
- **Updates**: daily check for new versions and installation offered in one click.
- **Claude**: use of Claude Code and the Claude subscription, with no API key.

---
type: index
tags:
  - meta
---

# Workflow

## The loop

```
capture  ->  00. Fleeting Notes     (seconds. no structure. no judgement.)
   |
read     ->  01. Source Material    (one note per source. claims + MY reading.)
   |
think    ->  04. Zettelkasten       (one idea. own words. >=2 links. ID-named.)
   |
find     ->  02. Indexes            (MOC when a cluster gets too big to hold in head.)
```

## Rules

**1. One idea per permanent note.** If a note needs "and" in its title, it is two notes.

**2. Own words, full sentences.** A quote is not a thought. Copy-paste belongs in `01. Source Material`, never in the slip-box.

**3. Two links minimum, written at creation.** Not later. Later never comes. A note with no links is a note you will never find again. The folder is not the index. The links are.

**4. Say *why* on every link.** `[[note]] — contradicts this` beats a bare `[[note]]`. The reason is the actual knowledge.

**5. A literature note stays complete.** Claims hold what the author argues. Detail that is not a claim, such as timelines, numbers and terminology, goes in a Background section rather than being cut. Deleting detail from a source note means going back to the source to get it again, which costs more than the space it saved.

**6. Fleeting notes expire.** Process within a week or delete. A fleeting note you keep "just in case" is clutter you will never read.

**7. The slip-box stays flat.** Never make subfolders in `04. Zettelkasten`. Structure comes from links and MOCs, not from directories.

**8. Write the note you would need in five years,** not the one that makes sense today with the source still open.

## Mechanics

| Action | How |
|---|---|
| New permanent note | Command palette → *Create new unique note*. Gets a `YYYYMMDDHHmm` ID. |
| New fleeting note | Ctrl/Cmd+N. Lands in `00. Fleeting Notes`. |
| New literature note | New file inside `01. Source Material`. |
| New daily log | Command palette → *Open today's daily note*. |
| New chapter | Command palette → *Templater: Create new note from template* → Chapter Draft. |

Templater fills the template by folder, so the first four need no template command. Tab jumps between the fields it left for you.

`04. Zettelkasten`, `01. Source Material` and `00. Fleeting Notes` each have a folder rule. `06. Projects` deliberately does not, because an outline and a chapter want different templates.

IDs are timestamps and never change. **Titles can be renamed freely.** Obsidian rewrites links.

## Prose rules

Rule 2 says own words. These say which words.

**No metaphor as a substitute for the claim.** One image to illuminate a stated point is fine. An image standing in place of the point is not. If the metaphor were deleted, the sentence should still say something.

**No explaining what you just said.** Say it once. A follow-up sentence beginning "In other words" or "What this means is" means the first sentence failed. Fix the first sentence.

**No brochure language.** Cut "powerful", "seamless", "robust", "leverage", "unlock", "deep dive", "at its core". These describe nothing and survive only because they sound like writing.

**No synonym roulette.** Name a thing, then keep that name. Switching to "the tool", "the platform", "the solution" to avoid repetition makes the reader check whether you changed subject. Repetition is clearer.

**Use "is" and "are".** Not "serves as", "functions as", "represents", "constitutes", "acts as". A fancy verb where a copula belongs adds syllables, not meaning.

**No "not just X, but Y".** Also "isn't merely", "more than just". The formula manufactures depth by denying a claim nobody made. State Y.

**No mechanical threes.** Three parallel items because three sounds complete is padding. Use the number of items that exist.

**No decorative dashes.** A dash marks a genuine break or aside. Used for rhythm, it becomes noise and every sentence starts to sound the same. Prefer a period or a colon.

**No robotic phrasing.** Cut "it is important to note", "it should be mentioned", "delve into", "navigate the complexities", "plays a crucial role in". If a sentence would read identically with the phrase removed, remove it.

Applies to permanent notes above all. A permanent note is read by someone who has forgotten the context, and padding is what makes it unreadable.

## Projects

The slip-box is written for you and has no deadline. A project is written for readers and has both a deadline and a shape. Keep them apart.

`06. Projects/<name>/` holds everything that dies when the project ships: outlines, drafts, API details, snippets, todo lists. Scrappy is fine there. None of the rules above apply.

Two things cross the boundary.

**Into the slip-box.** Working on a project makes you notice things that stay true after it ships. Where you got stuck. What a source assumed you already knew. Why one explanation order works and another loses people. Write those as permanent notes. They are usually the best notes you will ever write, because nobody else can observe your own confusion.

**Out of the slip-box.** When you draft, pull the relevant permanent notes and arrange them. A draft is an arrangement, not a first writing. If the slip-box is empty at draft time, you are writing from scratch every time.

Mechanics stay in the project folder. "requestAdapter returns null when there is no GPU" goes in `06. Projects`, never in `04. Zettelkasten`, because the API will change and the note will quietly become wrong.

**Close the loop once, not twice.** A chapter links the sources and permanent notes it was built from. The source note does not link back, because Obsidian already shows that under backlinks. Hand-maintained reverse links go stale the first time you rename something.

**A project ends.** Archive or delete the folder. Anything worth keeping already moved into the slip-box.

## Promoting a fleeting note

1. Read it. Still interesting? If no → delete, no guilt.
2. Create a unique note in `04. Zettelkasten`.
3. Rewrite the idea in full sentences, standalone, no context from the original.
4. Link two existing notes, with reasons.
5. Delete the fleeting note.

---
Back to `[[Home]]`.

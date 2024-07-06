# Change Log

All notable changes to the "mtg-code" extension will be documented in this file.

## [Unreleased]
<!-- The `blockquote`s under the `li` are just notes for development. They may or may not be included in the release's changelog. -->
- Deck stats in custom panel
  > * Show counts for creature/noncreature/land, colors, subtypes, etc.
  > * Selecting an item from the panel highlights the lines with cards that have that property/quality.

<!-- collapsible "proposed features" section -->
<style>
  details {
    --clr-bg: #B1C2D3;
    background-color: rgb(from var(--clr-bg) r g b / 0.1);
    padding: 0.75em;
    margin-bottom: 1em;
    summary h2 {
      display: inline-block;
    }
  }
</style>
<details>
<summary>

## [Proposed]
</summary>

### Add
- Recognition for deck files vs. scratch.
- Conversion between different deck formats.
- Deck legality checking
- Action to upload deck to deckbuilding site.
  > On success, append a comment to the deck file with a link to the online decklist, if possible.
- Action to open a scryfall search in the browser
- Action to open a card in Gatherer. (and other search engines? are there any?)
- Ability to set "search context" when deckbuilding
  > i.e. set options for `format`, `colors`, etc. that would be included in all searches made from the current deck file's editor.
- "Code Suggestion" actions (`Ctrl + .`) that would trigger searches for related cards.
  > Examples: Other red cards, Other 1 mv cards, Other cards with flying.
- Other deck views, i.e. show images in fanned-out stacks by mana cost with badges showing the number of copies of that card.
- Simplified deck probability info (probably another custom panel).
  > * Initially, this would ignore card draw, ramp, and other resource requirements (e.g. needing a creature to tap so the land makes mana of any color).
  > * The model should take into account if the land comes into play tapped.
  > * **Probabilities to compute:**
  >   * ***P**(drawing CARDNAME by turn X)*
  >   * ***P**(drawing CARDNAME by turn X && having enough mana to cast it)*

<!-- ### Change -->

<!-- ### Deprecate -->

<!-- ### Remove -->

<!-- ### Fix -->

<!-- ### Security -->

</details>

## [1.1.1] - 2023-11-07
### Added
- Show total price of cards in euros and usd in selection in the status bar.

### Fixed
- Syntax highlighting in search lines now works with negation.
- Local card database is now stored in the global storage URI provided by VSCode.

## [1.1.0] - 2023-03-04
### Added
- Show average converted mana cost of cards in selection in the status bar.
- Folding ranges for all blocks starting with a comment line (comment or search line).
- Command to show a card's rulings.
- Syntax highlighting support for *'or'* and parenthesis.

### Fixed
- Syntax highlighting for quoted fields.
- Prevent the extension from breaking in case new fields are added to scryfall's API.

## [1.0.2] - 2022-04-22
### Fixed
- Fixed card parsing for cards which included a 'penny_rank' field.


## [1.0.1] - 2022-04-22
### Fixed
- Fixed card parsing by adding the explorer format.

## [1.0.0] - 2022-02-28
### Added
- Syntax highlighting for deck lists, comments and search lines.
- Autocompletion for card names while typing in deck list.
- Card preview, including a small image and card prices, when hovering a card in the decklist.
- Card search using scryfall's advanced query API.
- Autocompletion for query terms and for some query parameter values in card search lines.
- Display card count when selecting multiple lines.

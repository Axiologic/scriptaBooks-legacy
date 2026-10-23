# ScriptaBooks Legacy

Ten additional ScriptaHub books in their original published layout, for testing compatibility with ScriptaHubAgent. These IDs do not overlap with scriptaBooks-1.

## Layout

```text
collection.json
books/<original-title-path>/bk-<original-id>/
  manifest.json
  editions.json
  en/book.html
  en/full_content.html
  en/short_content.html
  en/book.pdf
  <language>/...
  edition-files/...
  Animation/...
```

The repository root corresponds to the original ScriptaHub `docs/` publishing root. Original book directories, filenames, generated pages, edition history, translations and duplicate assets are copied unchanged. Formats vary by book; the catalog advertises the original resources. Shared application assets, the reader and forms are provided by ScriptaHubAgent.

`collection.json` uses the original schema version 1 and contains only these ten book records. Keyword counts are recomputed for this subset. It does not use the deduplicated version 2 layout of scriptaBooks-1.

## Books

- 100 Dangerous Questions: Breaking Free from the Web of Control and Deception (`bk-dd18acafe4c142df`)
- A Balance of Iron and Salt (`bk-bc50aebc325a41a6`)
- A Cheeky Guide to Ancient Greek Philosophy (`bk-1bcfe492ede446ee`)
- A Drive into the World of the Hunger Games (`bk-00322966cb714b73`)
- A Glimpse into Frank Herbert’s Dune (`bk-e3cf68155b524bf6`)
- A Humorous Take on Mary Shelley’s Frankenstein (`bk-d6eaef63e21e4c47`)
- A Hundred Years of Solitude Unbound (`bk-175ac501007a4e50`)
- A New Era of Finance: The Bitcoin Standard (`bk-62b1d1973f6d45e1`)
- A Quick Guide to Notorious Conspiracy Theories (`bk-eafc0608eb5d421b`)
- A Report on Secret Societies and Real Conspiracies (`bk-a3ad60f35a134e75`)

## Source and verification

Copied from [Axiologic/ScriptaHub](https://github.com/Axiologic/ScriptaHub) commit `9fade75c2948d9a77a559d156134f76ee0b5d051`. All 492 copied book files (177,561,213 bytes) were checked against their original Git blob hashes. The source repository is unchanged.

## Agent configuration

Add this URL to `repositories` in ScriptaHubAgent `sources.json`:

```json
"https://raw.githubusercontent.com/Axiologic/scriptaBooks-legacy/master/collection.json"
```

The agent reads the configured JSON URL over HTTP and streams the original files on demand. It does not clone this repository. Original public paths remain valid under the agent base URL.

# 創業島探索者 · 香港創業島 / HK Startup DAO

A small, instruction-only skill for co-hosts to prepare fresh topics and
60-minute conversations. No plugin, scripts, API keys, database, or background
service. Start with [SKILL.md](SKILL.md).

## For hosts / 主持人使用方法

Copy this prompt into an assistant that can read web pages or repository files:

```text
請閱讀以下《香港創業島》節目策劃 skill：
https://github.com/szewong/hkstartupdao-show/blob/main/SKILL.md

請一併閱讀 SKILL.md 指定嘅 references 檔案，按照節目定位幫我準備今週節目。
查閱最新 Apple Podcasts / Spotify 節目，避免重複最近講過嘅角度。
建議三個題目，揀一個，並準備適合四至五位主持嘅 60 分鐘 rundown。
簡短講明你實際讀到邊啲資料；讀唔到或未核實嘅資料請直接講明，唔好估。
```

Raw Markdown alternative:
https://raw.githubusercontent.com/szewong/hkstartupdao-show/main/SKILL.md

The assistant must read the entry file and all three active references, not just
the repository homepage. Relative links are relative to SKILL.md. A pasted link
is a read-and-follow workflow, not installation or a guarantee of access.

For a different task, simply request it: “只要五個題目，暫時唔使 rundown”;
“將第二個題目寫得更口語”; or “今次得四位主持，改成 45 分鐘.”

If web access fails, attach SKILL.md and the three files in references/.
The assistant can use the snapshot but must disclose when it cannot check new
releases. It must not pretend it has read or watched inaccessible material.

## Files

```text
hkstartupdao-show/
├── README.md
├── SKILL.md
├── .gitignore
└── references/
    ├── sources.md
    ├── past-episodes.md
    └── topic-backlog.md
```

- **SKILL.md:** editorial voice, source checks, fresh angles, and a timed rundown.
- **sources.md:** Spotify/Apple links, reading order, and coverage limitations.
- **past-episodes.md:** a dated 12-entry podcast snapshot and 50 older YouTube
  records. These may overlap; they are not 62 confirmed unique episodes.
- **topic-backlog.md:** an empty template for ideas approved for public release.

The audience is Hongkongers around the world. Default output uses Traditional
Chinese and natural Cantonese, with practical, lively discussion for 4–5 hosts.
Avoiding repeats means comparing the central question and takeaway, not merely
the title. Revisit a broad subject only with a genuinely different angle.

## Public repository / 私人資料

**This repository is public.** Unpublished ideas, personal scheduling notes,
unverified historical planning logs, and the original source archives were not
uploaded. The original prepared package remains separate and unchanged.

Do not add host-only planning material without explicit approval for public
release. Use a separate private workspace for it. The .gitignore exclusions are
only a convenience, not an access-control system. No license file has been added.

## Maintenance

The included snapshot was collected during preparation on **2026-10-01**; it was
not refreshed during upload. It is a fallback, not a live database. Ask the
assistant to check the live podcast listings for every new planning session.
Apple and Spotify copies of one episode count as one release.

After an episode is published, a host can explicitly request an update with the
final title, public URL, known publication date, and main discussion angle.
Unknown dates stay unknown. A draft is not an aired episode. Changes reach GitHub
only after a real repository write; the skill does not synchronize itself.

## Portable use

For a client that supports the SKILL.md format, supply the entire
`hkstartupdao-show` folder, including references/. Follow that client's own
installation instructions; copying only SKILL.md leaves its references missing.
For the initial test, explicitly asking the assistant to read these files is
sufficient when it has file/web access. No plugin installation is required.

## Acceptance checks

These are prompts for a host's first runtime test, not claims of completed
end-to-end tests:

| Prompt / condition | Expected behavior |
| --- | --- |
| 今週三個 topic，揀一個做 rundown | Reads references and available current sources; three distinct ideas; one 60-minute rundown |
| 想再講 Local AI | Identifies relevant recent coverage and explains the new angle or flags a repeat |
| 只要五個中文標題 | Five titles without an unwanted full rundown |
| 得四個主持，45 分鐘 | Four roles and continuous timings totaling 45 minutes |
| Podcast access fails | Dated coverage limitation; no claim of a complete current scan |
| Save an unpublished idea | Checks public-release intent; does not silently expose private planning |

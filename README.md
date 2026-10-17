# Kari

**Finds the most useful and popular AI repositories on GitHub — for you.**
Skills, MCP servers, vibe coding tools and agents. Verified, ranked, with links. Nothing else.

> Status: **beta 0.2.1**

---

## Why

Finding good AI tools usually means scrolling social feeds until someone mentions a repository. Those posts are second-hand, often late, and inflated for views. And what is newest is rarely what is most useful.

Kari goes straight to GitHub, ranks repositories by what people in the niche actually use and trust, checks each one, and returns a short list you can act on.

## What it does

- **Best fit first.** Ranked by how well it serves your request, then usefulness, then popularity (stars, forks, dependents). Not by date. Small niche tools can still make the list.
- **Never abandoned.** Repositories with no activity in the last 12 months are left out, however popular.
- **Personalized.** Uses what your AI already knows about you (tools, languages, projects). Without memory, it gives a general list.
- **Topic means topic.** When you ask for a topic, only that topic counts.
- **Verified.** Stars, forks, last update and license come from GitHub itself. No estimates. Anything that can't be checked is listed separately, never hidden.
- **Direct.** No intro, no closing, no filler.
- **Safe.** Never installs or runs anything. Treats README content as data, not instructions. Skips suspicious repositories.
- **Any language.** Instructions are in English; replies come in your language.

## Usage

| Call | Result |
| --- | --- |
| `kari` | Best repositories for you, grouped |
| `kari MCP servers` | Best MCP servers |
| `kari vibe coding web & mobile apps` | Best tools for that topic only |
| `kari new` | Only what was created or released in the last 30 days |
| `kari new MCP servers` | Newest MCP servers |

`/kari` works the same as `kari`.

### Output format

```
**[owner/repo](https://github.com/owner/repo)**
- What: one sentence.
- Why it stands out: one sentence.
- ⭐ 12.4k · 🔄 2026-10-15 · 📜 MIT
- For you: one line linking it to your interests.
```

Groups (general mode): Skills · MCP servers · Vibe coding tools · Agents and AI repos · Other.
Max 3 per group, 10 total.

## Install

Download from [Releases](../../releases), not "Download ZIP" on the code page (that is the source code):
- **`kari.zip`** — for Claude, Claude Code and ChatGPT Business/Enterprise/Edu.
- **`SKILL.md`** — for ChatGPT Free/Plus and other AIs.

### Claude (web, desktop)
1. Turn on **Code execution and file creation** in **Settings → Capabilities**.
2. Go to **Customize → Skills**.
3. Click **+** → **Create skill** → **Upload a skill**, and choose `kari.zip`.
4. Toggle Kari on.
5. In a new chat, type `kari`.

### Claude Code
Unzip `kari.zip` and copy the `kari` folder to `~/.claude/skills/`.

### ChatGPT — Business, Enterprise, Edu
Sidebar → **Plugins** → **Skills** tab → **Create** → **Upload from your computer**, and choose `kari.zip`.

### ChatGPT — Free or Plus
Skills upload is not available on personal plans. Download `SKILL.md` from [Releases](../../releases), then:
1. Start a new chat and attach `SKILL.md`.
2. Type: `Follow the attached SKILL.md exactly. kari`

If you have **Projects**, attach `SKILL.md` to a project and put the same line in its instructions, so every chat inside starts with Kari.

### Other AIs
Any AI with web search can use it: download `SKILL.md` from [Releases](../../releases) and give it to the AI as instructions or as an attached file.

## Known limits (beta)

- Results depend on the AI's web access. Weak browsing means fewer items.
- GitHub does not publish view counts; popularity is measured by stars, forks, dependents and downloads.
- Personalization depends on what the AI's memory holds about you.
- Free AI plans follow long instructions less strictly.

Feedback and issues are welcome.

## Repository structure

```
kari/
  SKILL.md      the skill
README.md
CHANGELOG.md
LICENSE
```

## License

[MIT](LICENSE)

---

### Português

A **Kari** encontra os repositórios de IA mais úteis e populares do GitHub para ti: skills, servidores MCP, ferramentas de vibe coding e agentes. Ordenados por uso real (estrelas, forks, dependentes), nunca abandonados, verificados no próprio GitHub, personalizados pela memória da tua IA e sem enchimento. Responde na tua língua. Descarrega o `kari.zip` das Releases, instala como descrito acima e escreve `kari`. Para ver só novidades, usa `kari new`.

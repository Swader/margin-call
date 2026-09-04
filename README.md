# Margin Call

An agent skill for clear replies that take less effort to read.

> "speak to me as if to a young child or, perhaps, a golden retriever"

The brief takes its name from *Margin Call*. It asks for simple explanations with respect for the reader.

## What it does

- Applies ASD-STE100 Simplified Technical English to all replies, including work updates, questions, and final answers.
- Puts the answer first and makes the next action clear.
- Uses short sections and visible task state to help readers with ADHD.
- Uses literal statements instead of decorative metaphors and clever phrases.
- Keeps facts, warnings, and necessary detail intact.

It does not shorten the work itself. Code and exact quotes keep their original text.
Read [SKILL.md](SKILL.md) for the full instructions.

## Install in Codex

Clone this repository into your personal skills folder:

```sh
git clone https://github.com/swader/margin-call.git ~/.agents/skills/margin-call
```

If your setup uses `~/.codex/skills`, use that folder instead. Install only one copy.
Do not replace an existing folder without checking its contents.
Restart Codex if the new skill does not appear.
Refer to the [official skill guide](https://learn.chatgpt.com/docs/build-skills) for discovery and installation details.

## Use

```text
$margin-call Explain why this test failed.
```

The skill allows automatic selection. To request it for every reply, add this line to your agent instructions:

```text
Always use the margin-call skill when speaking to me.
```

The skill keeps its style across turns after activation. Installation alone does not guarantee selection in every task.

## Example

Before:

> The upload operation could not be completed because the server rejected the API key. Please verify that the key belongs to this project.

After:

> The upload failed. The server rejected the API key. Check that the key belongs to this project.

## Sources and limits

The communication principles draw on [r13i's TLDR skill](https://github.com/r13i/skills/blob/main/tldr/SKILL.md).

[ASD-STE100](https://www.asd-ste100.org/) supplies the language standard. The standard includes writing rules and a controlled dictionary.
This skill gives practical instructions; it does not include the complete standard or certify compliance.
ASD owns the standard and its trademarks. This project does not claim ASD endorsement.

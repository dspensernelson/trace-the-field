# Trace the Field

An interactive map of how one data field travels through an AI-assisted build: from the seed value someone picks, through the agent that writes it, into the list that stores it, to the line it fills in the finished output.

**Live page:** https://dspensernelson.github.io/trace-the-field/

The example is a monthly AI newsletter for a fictional firm, Contoso Consulting, built on Copilot Studio agents, SharePoint lists, a Power App, and Power Automate flows. Names, links, and IDs are placeholders, and most of the text is lorem ipsum. The structure, field names, and wiring are the point.

## The idea

Click any field and its whole path lights up. Lines that stop short are the build list:

- **Gold "add"** marks a field that is planned but not built yet.
- **Red "fix"** marks a field that is built but does the wrong thing.
- **A dead-end line** means something writes a value nothing receives, or needs a value nothing writes.

Every piece carries one ID, the same on every tab, so a box in the trace can be found on the process map, the flows canvas, or the build schedule.

## Tabs

| Tab | What it shows |
| --- | --- |
| Trace the field | The field-lineage board described above |
| Flows | The Power Automate flows as a node canvas |
| Agents | Each agent's instructions, outputs, and test briefs |
| Prompt drafts | Ten starter prompts for the prompt library |
| SharePoint | The lists and their columns |
| Process map | The whole process as one diagram |
| Build schedule | Build steps, status, and open questions |
| Screen 1, Screen 2 | Power App screen mockups |
| The email | The finished newsletter the system produces |
| Gap check, Practice run | Coverage check and a dry run of one issue |

## Files

- `index.html` is the whole page, self-contained.
- `data/` holds the Flows, Agents, and Prompt drafts content as JSON. The page embeds the same data, so it works offline. Edits made in those tabs are not saved.

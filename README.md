# Open ACH

**Analysis of Competing Hypotheses, in your browser.** List every plausible explanation, rate each piece of evidence against all of them, and favor the hypothesis with the least evidence *against* it.

**Use it:** https://jc0h3n.github.io/open-ach/

ACH was developed by Richards J. Heuer Jr. at the CIA to counter confirmation bias, the habit of settling on one explanation and then mostly noticing the evidence that fits it. Open ACH is a modern, private, free implementation of the method.

## Features

- **Matrix:** hypotheses as columns, evidence as rows, rated from Very consistent (CC) to Very inconsistent (II), with credibility and relevance for every item
- **Weighted inconsistency scores:** hypotheses ranked by the evidence against them, updated as you rate
- **Diagnosticity:** marks which evidence actually helps tell hypotheses apart, and flags items that don't. You can sort the matrix by it.
- **Sensitivity analysis:** finds the evidence your conclusion hinges on, meaning items whose removal would change which hypothesis leads
- **Guidance:** next-step prompts tied to Heuer's 8 steps, plus a full guide and a worked example
- **Report and export:** conclusion and milestones, with export to a Markdown report, a CSV matrix, or a JSON analysis file you can reopen or share
- **Private by design:** analyses are saved only in your browser. There are no accounts, servers, fonts, analytics or third-party scripts.

## How the scores work

Each Inconsistent rating counts 1 point against a hypothesis and each Very inconsistent rating counts 2. Each point is multiplied by the evidence's credibility and relevance (Low 0.5, Medium 1, High 1.5). Lower totals mean fewer and weaker reasons to reject the hypothesis.

Consistent ratings add nothing, because evidence that fits several hypotheses can't help you choose between them. That is Heuer's central point. The scores support judgment; they don't replace it. The Guide in the app explains diagnosticity and sensitivity in detail.

## Running it locally

Plain HTML, CSS and JavaScript modules, with no build step. Serve the folder with any static server and open it, for example:

```
npx serve .
```

## Credits

- Method: Richards J. Heuer Jr., [*Psychology of Intelligence Analysis*](https://www.cia.gov/resources/csi/books-monographs/psychology-of-intelligence-analysis-2/) (CIA Center for the Study of Intelligence, 1999), chapter 8
- Inspired by the collaborative open-source ACH by Matthew Burton and Joshua Knowles: [Burton/Analysis-of-Competing-Hypotheses](https://github.com/Burton/Analysis-of-Competing-Hypotheses) (2010). Open ACH is a new codebase and shares that project's license.

## License

[GNU General Public License v3.0](LICENSE)

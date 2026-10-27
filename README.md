# Quorum: open review for preprints

Fast public review, weighted by who actually knows the field.

**Live demo:** https://ninamarie-zinke.github.io/quorum-demo
*(All people, reviews, and results are synthetic.)*

Built at the Claude Impact Lab: Biotech & Life Sciences (San Diego, Oct 26, 2026), Track 2: in silico testing and discovery.

## The problem

Preprints move fast, but meaningful feedback is slow and uneven. When every vote counts the same, popularity can drown out real expertise.

## What Quorum does

1. **Structure:** Reviewers fill out one six-field form (claim, stance, point, evidence, requested revision, testable hypothesis, plus confidence).
2. **Score:** Each review gets a credibility score from three signals:
   - Field expertise (field-normalized citation impact, RCR)
   - Topic match (how close the reviewer's own papers are to this one)
   - Review substance (cites evidence, targets a specific claim, proposes a test)
3. **Rank:** Credibility comes first. Votes are shown alongside but never enter the score.
4. **Synthesize:** Each claim becomes a testable hypothesis, traced to the most credible named review.
5. **Send:** Authors receive a revision packet (Markdown email or JSON).
6. **Credit:** Accepted reviewers can be added to the paper with an asterisk, at the authors' discretion.

The page includes a self-test and adjustable scoring weights, so you can see how the ranking changes.

## Limitations

- Quorum ranks who to listen to first. It does not decide what is true.
- Everything in the demo is synthetic. In production, RCR would come from NIH iCite, topic match from reviewer abstracts, and substance from Claude. In the demo, new reviews get a simple structure score instead.
- RCR is still citation-based, so well-known labs can still rank high with weak comments.
- Unverified reviewers are scored on their text alone and are always tagged.
- Votes measure popularity, not quality, which is why they don't affect ranking.
- Journals set their own authorship rules. Quorum only records the decision.
- The self-test was written by our team. Real validation needs a hold-out set labeled by independent domain experts.

## Run it locally

It's a single self-contained file. Open `index.html` in any browser.

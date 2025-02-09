# RefNLI

This is the official repo for "On Reference(In-)Determinacy in Natural Language Inference" in NAACL 2025 Findings. 

## Dataset & Format

RefNLI features 1,143 examples of NLI (premise, hypothesis) pairs, where the entailment relation involves judgements on whether the hypothesis and premise refer to the same context. 
Unlike the usual 3-way NLI labels, RefNLI features the following 4-way label set. 

- `Entailment`: If the human annotator thinks that the premise and hypothesis likely refer to the same context, and the premise is sufficient to fully support the hypothesis.
- `Contradiction`: If the human annotator thinks that the premise and hypothesis likely refer to the same context, and the hypothesis is unlikely to be true given the premise.
- `Ambiguous`: If it is unclear whether the hypothesis and the premise refer to the same context (e.g., contain ambiguous references), and there exist multiple possible assignments or interpretations of references that could make the example fall into at least two of the other three labels.
- `Neutral`: If it is clear that the premise cannot support or contradict the hypothesis in any way, i.e., there exists no interpretation or assignment of references of the premise where it can support or contradict the hypothesis.

| Hypothesis                                         | Premise                                                                                                           | RefNLI Label       | NLI Model prediction |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|------------|---------------|
| Sabbir Khan made his directorial debut in 2001.   | In 2009 he made his directorial debut with the film “Kambakkht Ishq” (2009) that starred Akshay Kumar and Kareena Kapoor. | Ambiguous  | Contradiction |
| Wales has a large region rich in coal deposits.   | Recent explorations have revealed prospective deposits of rare-earth elements, a company is proposing further analysis of these mineral deposits. | Neutral    | Contradiction |
| Same Old Love is a work of music.                 | “Same Old Love” was also performed on “The Ellen DeGeneres Show”, “The Tonight Show Starring Jimmy Fallon”, 2015 American Music Awards, and at the 2015 Billboard Women in Music. | Entailment | Contradiction |
| Buffy the Vampire Slayer is exclusively a Japanese television series. | “Buffy the Vampire Slayer” comics refer to comic books based on the television series “Buffy the Vampire Slayer” | Contradiction | Entailment |

## Citation
```
@inproceedings{chen2025reference,
  author    = {Sihao Chen and Chaitanya Malaviya and Alex Fabrikant and Hagai Taitelbaum and Tal Schuster and Senaka Buthpitiya and Dan Roth},
  title     = {On Reference (In-)Determinacy in Natural Language Inference},
  booktitle = {Findings of the Association for Computational Linguistics: NAACL 2025},
  year      = {2025},
}
```

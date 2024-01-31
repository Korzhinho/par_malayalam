# par_malayalam
A dataset of paraphrases in Malayalam collected for the DravidianLangTech-2024 workshop at EACL 2024.

#### The Data
The dataset consists of candidate pairs of sentences in Malayalam. Each pair has a label 1 or 0 identifying the sentences as paraphrases or not, an English translation and the confidence in the label, based on the aggregation model (see below).
The labeling was conducted on the Toloka crowdsourcing platform.

#### Annotator Selection
The annotators where chosen based on:
- Knowledge of Malayalam, specified by the annotator in their Profile information
- Location: India, based on their profile information as well as the telephone number, used for registration.
- Top 90% of annotators, based on their overall quality of performance on the platform

#### Task Setup
Annotators who were eligible for the task, were given access to the pairs of sentences for binary annotation with a question: "Do these texts paraphrase each other?" and the Yes/No answer options.
Each pair was given to three random eligible annotators, and this overlap was used to aggregate the answers into the resulting labels with the Dawid-Skene aggregation model.
Overall, 31 annotator took part in the task.

#### Quality Control
The platform allows for different quality control rules, and the following ones were used:
- Fast Responses. The rule was banning annotators who submitted a set of five tasks in less than 15 seconds. The rule was used to avoid random clicking.
- Majority Vote. The rule was tracking the answers of the annotator against the answers of other annotators to the same task. With overlap 3 (see above) and accepted majority as 2, the rule calculated the percentage of the annotator's answers accepted as majority. The threshold of 80% accuracy was used to filter out annotators below it.

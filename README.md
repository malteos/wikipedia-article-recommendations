# Wikipedia Article Recommendations: A Qualitative Evaluation of User Preference for Link-based vs. Text-based Recommendations of Wikipedia Articles

This repository contains the supplemental materials for the ICADL 2021 paper [A Qualitative Evaluation of User Preference for Link-based vs. Text-based Recommendations of Wikipedia Articles](https://arxiv.org/abs/2109.07791):
- Questionnaire used for the user study
- Participants answers (transcripted interviews and quantitative data)
- Code to reproduce the figures in our paper

## User study design

![Wikipedia Relations](https://github.com/malteos/wikipedia-article-recommendations/raw/main/study-design.png)

Prior to our study, we created a sample of 40 seed articles covering a diverse spectrum of article types in Wikipedia.
Our aim when selecting these seed articles was to achieve a diversity of topics, which nonetheless remained comprehensible to a general audience.
To fulfil the requirement of comprehensibility, we excluded topics that would require expert knowledge to judge the relevance of recommendations, e.g., articles on mathematical theorems or regional historical events.
Moreover, the seed articles featured diverse article characteristics, such as article length and article quality, which we judged using Wikipedia's vital article policy.

We distinguished seed articles into four categories.
First, according to their *popularity* (measured by page views) into either niche or popular articles, and second, according to the content of the article into either *generic*, i.e. reference articles typical of encyclopedias, or *named entities*, i.e. politicians, celebrities, or locations.

We choose popularity as a criterion because, on average, popular articles receive more in-links from other articles.
Schwarzer et al. found that the number of in-links affected the performance of the link-based CPA approach.
Moreover, we expected study participants to be more familiar with popular topics compared to niche articles and therefore users will be better able to express their spontaneous information needs when examining a topic.

The "article type" categories were chosen to study the effect that articles about named entities may have on MLT.
Names of entities tend to be more unique than terms in articles on generic topics. Therefore, we expect that specific names may affect MLT's performance.
Likewise, due to the nature of Wikipedia links to generic topics, they may appear in a broader context than links to named entities.
Thus, CPA's performance may also be affected.
These considerations resulted in four article categories:

- (A) niche generic articles,
- (B) popular generic articles,
- (C) niche named entities, and
- (D) popular named entities.

To perform our qualitative evaluation of user-perceived recommendation effectiveness, we recruited 20 participants.
Participants were students and doctoral researchers from several universities in Berlin and the University of Konstanz.
The average age of participants was 29 years.
65% of our participants said they spend more than an hour per month on Wikipedia, with the average being 4.6 hours spent on Wikipedia.

Our study contained both qualitative and a quantitative data collection components, i.e. mixed methods design. The quantitative component took the form of a written questionnaire.
This questionnaire asked participants about each recommendation set separately and elicited responses on a 5-point Likert scale.
Some questions were tailored to gain insights on the research questions we defined for our study, while the remainder of the questions adhered to the ResQue framework for user-centric evaluation.
The qualitative component took place as an interview.
This component contained open-ended questions that encouraged participants to compare the two recommendation sets.
The participants were asked to describe their perceived satisfaction.
Resulting from this design, we could use the qualitative semi-structured interviews to interpret and validate the results from our quantitative questionnaires.
The qualitative interviews were audio-recorded with the permission of our participants.

In the study, each participant was shown four Wikipedia articles, one at a time.
For each article, two recommendation sets, each containing five recommended articles, were displayed.
One set was generated using CPA, i.e., the link-based Citolytics implementation, while the other was generated using the MLT algorithm.
Each set of four Wikipedia articles was shown to a total of two participants to enable checking for the presence of inter-rater agreement.

Participants were aware that recommendation sets had been generated using different approaches, but they did not know the names of the approaches and the method behind the generation, or on which side below the seed article which recommendation set was being displayed. We alternated the placement to avoid the forming of a potential bias.
The seed Wikipedia articles were shown to participants via a tablet or a laptop.
The participants were asked to read and scroll through the full article so that the exploration of the article's content was a natural as possible.

## Evaluation data

The evaluation data can be found in `./data`.

## Code

Follow these instructions to reproduce the figures from our paper.

### Requirements

- Python 3.7+ (Conda)

### Installation

Create a new virtual environment for Python 3.7 with Conda:

```bash
conda create -n paper python=3.7
conda activate paper
```

Clone repository and install dependencies:

```bash
git clone https://github.com/malteos/wikipedia-article-recommendations.git repo
cd repo
pip install -r requirements.txt
```

### Figures

Start the Jupyter notebook and execute all cells to generate the figures:

```bash
jupyter notebook paper_evaluation.ipynb
```

## How to cite

If you are using our code, please cite [our paper](https://arxiv.org/abs/2109.07791):

```bibtex
@InProceedings{Ostendorff2021b,
  title = {A Qualitative Evaluation of User Preference for Link-based vs. Text-based Recommendations of Wikipedia Articles},
  booktitle = {Proceedings of the 23rd International Conference on Asia-Pacific Digital Libraries (ICADL 2021)},
  author = {Ostendorff, Malte and Breitinger, Corinna and Gipp, Bela},
  year = {2021},
  month = {Dec.},
}
```


## License

MIT

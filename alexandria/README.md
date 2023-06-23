# Alexandria Index

The Alexandria Index is a dataset of vector embeddings of 2.25 million papers from arXiv using the the [`Instruct-XL`](https://huggingface.co/hkunlp/instructor-xl) model. The embeddings are 784-dimensional `float32` vectors. To run the notebook, you need to download the dataset, at <https://alex.macrocosm.so/download>.

Instead of running it yourself, you can just read some amusing things I found at the arXiv dataset. With 2.25 million papers, there are surprisingly very few amusing things to be found, speaking to the quality of arXiv.

## Odd abstracts

By looking at the duplicated abstracts, I found these oddities.  You can look at them yourself in `output_abstracts.txt`.

* Literally the same title and abstract, but one is longer than the other. <https://arxiv.org/abs/1907.05261>, <https://arxiv.org/abs/2006.13685>
* <https://arxiv.org/abs/2012.12178> is an extended abstract of <https://arxiv.org/abs/2104.09611>.
* <https://arxiv.org/abs/2303.04075> is an "evolved version" of <https://arxiv.org/abs/2209.12285>. Why couldn't they have submitted a second version?
* 500 papers withdrawn. Voluntary withdrawals are usually due to mistakes that invalidate the result, or the paper being superceded by later publications. The involuntary ones are usually due to plagerism or being a jerk. Notable examples:
    * 7 papers by N. Mebarki, A.Maireche are all plagerized.
    * 8 papers by Ramy Naboulsi, all plagerized. The situation was apparently that Naboulsi was trying to get into Japan. As a result we got probably the [weirdest abstract](https://arxiv.org/abs/hep-ph/0304045) ever, which is just an email from Yasushi Watanabe apologizing... The whole situation is described in [Preprint server seeks way to halt plagiarists | Nature](https://www.nature.com/articles/426007a).
    > The plagiarism case traces its origins to June 2002, when Yasushi Watanabe, a high-energy physicist at the Tokyo Institute of Technology, was contacted by Ramy Naboulsi, who said he was a mathematical physicist. Naboulsi asked for Watanabe's help in obtaining a research position in Japan. Impressed by Naboulsi's work, Watanabe agreed to upload some of his papers to ArXiv, which Naboulsi was unable to do himself as he had no academic affiliation. “I was so amazed at his productivity I began to think he was a genius,” Watanabe later wrote in an e-mail to the archive.
    * 3 papers by Tomasz Bodziony all about how Einstein faked his relativity papers. "withdrawn by arXiv administrators due to inflammatory content and unprofessional language".
    * 3 crackpot math papers by Asia Furones, "withdrawn by arXiv admin because of the use of a pseudonym, in violation of arXiv policy".
    * D. L. Khokhlov voluntarily withdrew 4 papers "due to the presented idea is wrong". Just the direct approach, huh?
    * 21 voluntary withdrawals due to "crucial sign error", 10 due to "crucial error".

Bonus arXiv trivia:
* <https://arxiv.org/abs/1511.08771>: 11232 pages long. The main text is 102 pages long. The rest of it is basically what happens when someone has a csv file but wants to squeeze it into a pdf.

## Odd titles

By looking at the duplicated titles, I found these oddities. You can look at them yourself in `output_titles.txt`.

Some really popular titles:
* 13 "Beyond the Standard Model"
* 9 "Physics beyond the Standard Model"
* 6 "Chiral perturbation theory"
* 6 "CP Violation in Hyperon Decays"
* 5 "CP violation"

Some papers are not informative: 2 "Title Redacted", 2 "withdrawn", 6 "Rejoinder".

Some uncommon title types:
* 73 starting with "Comment on" or "Comment:"
* 129 starting with "Discussion of" or "Discussion:"
* 11 "Matters of gravity", which turns out to be "The newsletter of the Division of Gravitational Physics of the American Physical Society".

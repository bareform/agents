# AGENTS.md

This file provides guidance to code agents when working with code in this repository.

## Repository Overview

```console
.
└── README.md
```

### README.md

This repository includes a `README.md`, a markdown file that describes what the codebase does, how to set it up, and how to use it. The `README.md` will follow the structure outline below.

#### Installation

```console
git clone https://github.com/bareform/dependencies.git
conda update -n base -c defaults conda
conda env create -f dependencies/environment.yml
conda activate bareform

git clone https://github.com/bareform/<repository-name>.git
cd <repository-name>
```
Replace `<repository-name>` with the name of the repository you are working in.

In the `details` HTML tag include any other major dependencies.
<details>
  <summary> Dependencies (click to expand) </summary>
  
  ## Dependencies
  - Python 3.10
  - Any other major dependencies
    
</details>

#### Quick Start

Start this section with the sentence "To train a low-precision `<dataset-name>` `<model-name>`:".

```console
python3 -m utils.trainer --config="./configs/<dataset-name>.toml"
```

Inspect `./configs/<dataset-name>.toml` to determine whether training is done in epochs or steps.
- ***If training is configured in epochs***, state: After training for `X` epochs, the results can be found at `./assets/<dataset-name>/<dataset-name>.png`.
- ***If training is configured in steps***, state: After training for `X` steps, the results can be found at `./assets/<dataset-name>/<dataset-name>.png`.

Replace `X` with the configured number of epochs or steps, as appropriate. 

Include the corresponding result image using the following Markdown-compatible HTML:

```html
<img src="assets/<dataset-name>/<dataset-name>.png" width="256" alt="<dataset-name>">
```

Conclude this section with the sentence "You can download the pre-trained models here and use the provided Jupyter Notebook `inference.ipynb` to generate some samples". Add a Markdown link to the word `here` to the link `https://huggingface.co/luethan2025/<repository-name>`.

#### Method

Add each item on their own line:
- The paper's full title as a Markdown link to its corresponding arXiv page.
- The authors' names, with numeric superscripts indicating their affiliations.
- The authors' affiliations, numbered to match the superscripts.

Conclude this section with a Markdown blockquote that contains the abstract from the arXiv page.

#### Citation

Start this section with the sentence "The original paper can be found at:".

Conclude this section with the following BibTeX citation.
```
@misc{First author's last name concatenated with the value in the year field concatenated with the repository name,
    title={Full title of the paper},
    author={Author's names seperated by the word `and`},
    year={Published year},
    eprint={arXiv identifier},
    archivePrefix={arXiv},
    primaryClass={Primary class}
}
```


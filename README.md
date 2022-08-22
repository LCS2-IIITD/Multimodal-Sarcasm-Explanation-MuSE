# Multimodal-Sarcasm-Explanation--MuSE-
This is the repository for "Nice perfume. How long did you marinate in it? Multimodal Sarcasm Explanation" accepted at AAAI-22. In this [paper](https://arxiv.org/abs/2112.04873), we propose a novel problem -- Multimodal Sarcasm Explanation (MuSE) -- given a multimodal sarcastic post containing an image and a caption, we aim to generate a natural language explanation to reveal the intended sarcasm. To this end, we develop MORE, a new dataset with explanation of 3510 sarcastic multimodal posts. Each explanation is a natural language (English) sentence describing the hidden irony. We benchmark MORE by employing a multimodal Transformer-based architecture, ExMore. It incorporates a cross-modal attention in the Transformer's encoder which attends to the distinguishing features between the two modalities. Subsequently, a BART-based auto-regressive decoder is used as the generator.

![MuSE Example](https://user-images.githubusercontent.com/18445035/145724756-149fcb7a-4687-4e5e-9e3f-8ac08a68fcce.png)

## Dataset
Dataset images can be found at this [link](https://drive.google.com/file/d/1CR3JIvatybTm3J3ZqLpZ4npq7OyHtcZf/view?usp=sharing).

The format of train, validation and test set TSV files:
* Column 1: PID, the identifier of a post
* Column 2: Caption, the text associated with the image in a post
* Column 3: Annotated explanation, the ground truth explanation for the sarcasm in a post

The image corresponding to a datapoint with, for example, PID=123 will be 123.jpg in the given link above.

## Model Weights
* Multimodal Sarcasm Detection pretrained checkpoint can be found [here](https://drive.google.com/file/d/1xiUJ1AHP5I07vAdV0cHvfigEnqDkYnXR/view?usp=sharing).
* ExMore model checkpoint can be found [here](https://drive.google.com/file/d/100NoUymoUlXZpjgcoSUa-A2l48tJWVzx/view?usp=sharing).

## Citation
If you find this repository useful, please cite our paper:
```BibTex
@misc{desai2021nice,
      title={Nice perfume. How long did you marinate in it? Multimodal Sarcasm Explanation}, 
      author={Poorav Desai and Tanmoy Chakraborty and Md Shad Akhtar},
      year={2021},
      eprint={2112.04873},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

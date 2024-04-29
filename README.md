**Audio Source Separation**

Emily Wang, Ohm Patel, Yilin Wang

**Introduction**

Motivation: Our project is based on the cocktail party problem. Based on real-life scenarios such as multiple people talking simultaneously at a party, this problem is often used to train and evaluate audio source separation models. Our models have a variety of applications such as separating political speakers speaking over one another and distinguishing a user’s voice from other people.

**Dataset**

We use the Librimix dataset for this project. Librimix is customizable dataset based on the the librispeech corpus and the WHAM noise dataset. In total, it has over 1000 hours of audio data consisting of clean and noisy overlapped audio of books read by different speakers. For this project, we will limit ourselves to clean audio rather than noisy audio.

https://github.com/JorisCos/LibriMix

How to access the data? Click on the link above

How to download the data? Clone the repo

How to set up the data in the repository? Run the main script : `[generate_librimix.sh](https://github.com/JorisCos/LibriMix/blob/master/generate_librimix.sh)`

(You do not have to upload the dataset to your GitHub repository, but you should include clear instructions on how to access the data, download it, and set it up in your repository.)

**Model**


- Data Preprocessing: Generating the Libri2mix dataset from the LibriSpeech corpus and the WHAM noise dataset. Augmenting samples by pitch shifting.
- Model: We plan to make architectural changes to an existing model called [ConvTasNet](https://arxiv.org/pdf/2010.15366v3.pdf).
- Audio Source Separation: The model provides us with 2 source separated audio clips.
- Transcript Generation: We use a pre-trained model on the separated audio clips to generate their transcripts.
- Evaluation: The performance metric that is most appropriate for this task is SI-SDR (Scale invariant- Source to Distortion ratio). It measures the ratio between the power of the source signal to the distortion introduced by the source separation.

(Explain the model architecture that your project uses. Be sure to include an architecture diagram here!)

**Using this Repository**

Please provide detailed instructions on how your codebase works. Ideally, someone should be able to recreate your model by following this guide.

**R**

**equirements**

Give instructions on setting up the environment.

```
conda env create -f environment.yml
conda activate hotdog

```

**Training the Model**

Explain how to train the model using the scripts in your repository.

```
python train.py

```

**Using the Model**

Explain how to use the model. Show a few examples in your `demo.ipynb`.

**References**

You **must** include references to any papers or GitHub repositories which you used when working on your project.

If you borrowed code from another GitHub repository, you **must** clearly write in your comments what is outsourced (and from where) and what is your own.

Huang, S.-F., Chuang, S.-P., Liu, D.-R., Chen, Y.-C., Yang, G.-P., & Lee, H. (2021). Stabilizing label assignment for speech separation by self-supervised pre-training. Interspeech 2021. https://doi.org/10.21437/interspeech.2021-763 


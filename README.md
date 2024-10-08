# Predict the intolerance of loss-of-function in human genes

#### Description
The model utilizes both gene expression and DNA sequence features to predict the intolerance of loss-of-function using a random forest-based (RF-based) approach.

#### Requirements
1.python == 3.8<br>
2.sklearn == 0.24.1<br>
3.pandas == 1.2.4<br>
4.Bio == 1.79<br>

#### How to run our code
</p>1. Please provide a fasta format file of your DNA sequence, with the gene symbol after &apos;>&apos; in the file.<br>
eg.<br>
>PF4<br>
ATGAGCTCCGCAGCCGGGTTCTGCGCCTCACGCCCCGGGCTGCTGTTCCTGGGGTTGCTGCTCCTGCCACTTGTGGTCGC
CTTCGCCAGCGCTGAAGCTGAAGAAGATGGGGACCTGCAGTGCCTGTGTGTGAAGACCACCTCCCAGGTCCGTCCCAGGC
ACATCACCAGCCTGGAGGTGATCAAGGCCGGACCCCACTGCCCCACTGCCCAACTGATAGCCACGCTGAAGAATGGAAGG
AAAATTTGCTTGGACCTGCAAGCCCCGCTGTACAAGAAAATAATTAAGAAACTTTTGGAGAGTTAG</p>
</p>
</p>2. Run Run prediction code:<br>
python predict.py -i examples/PSG.fasta -o result/result.csv <br>
-i: input file<br>
-o: output file<br>
</p>

#### Output file description
</p>1. The prediction column indicates the model's classification, where a value of 1 denotes a gene identified as essential for human individuals, and a value of 0 denotes a non-essential gene of human individuals. 
</p>2. The predict_proba column shows the probability that a particular sample is classified as an essential gene. This probability helps in assessing the confidence level of the classification provided by the model. If the predict_proba for a gene is greater than 0.5, the gene is classified as an essential gene. Conversely, if the predict_proba is 0.5 or lower, the gene is classified as non-essential.

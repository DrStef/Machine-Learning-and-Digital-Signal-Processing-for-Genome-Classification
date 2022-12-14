# ML-DSP-Machine-Learning-with-Digital-Signal-Processing-for-genome-classification

Project based on journal article:  
"ML-DSP: Machine Learning with Digital Signal Processing for ultrafast, accurate, and scalable genome classification 
        at all taxonomic levels."
Gurjit S. Randhawa, Kathleen A. Hill and Lila Kari


<span style="color:#4169E1">Randhawa et al. BMC Genomics (2019) 20:267
https://doi.org/10.1186/s12864-019-5571-y

1Department of Computer Science, University of Western Ontario, London,
ON, Canada
Full list of author information is available at the end of the article

<span style="color:#4169E1">The Abstract is reproduced here in-extenso: 

<span style="color: #7b241c"> "Background: Although software tools abound for the comparison, analysis, identification, and classification of
genomic sequences, taxonomic classification remains challenging due to the magnitude of the datasets and the
intrinsic problems associated with classification. The need exists for an approach and software tool that addresses the
limitations of existing alignment-based methods, as well as the challenges of recently proposed alignment-free
methods.
Results: We propose a novel combination of supervised Machine Learning with Digital Signal Processing, resulting
in ML-DSP: an alignment-free software tool for ultrafast, accurate, and scalable genome classification at all taxonomic
levels. We test ML-DSP by classifying 7396 full mitochondrial genomes at various taxonomic levels, from kingdom to
genus, with an average classification accuracy of > 97%.
A quantitative comparison with state-of-the-art classification software tools is performed, on two small benchmark
datasets and one large 4322 vertebrate mtDNA genomes dataset. Our results show that ML-DSP overwhelmingly
outperforms the alignment-based software MEGA7 (alignment with MUSCLE or CLUSTALW) in terms of processing
time, while having comparable classification accuracies for small datasets and superior accuracies for the large
dataset. Compared with the alignment-free software FFP (Feature Frequency Profile), ML-DSP has significantly better
classification accuracy, and is overall faster.
We also provide preliminary experiments indicating the potential of ML-DSP to be used for other datasets, by
classifying 4271 complete dengue virus genomes into subtypes with 100% accuracy, and 4,710 bacterial genomes
into phyla with 95.5% accuracy.
Lastly, our analysis shows that the “Purine/Pyrimidine”, “Just-A” and “Real” numerical representations of DNA
sequences outperform ten other such numerical representations used in the Digital Signal Processing literature for
DNA classification purposes.
Conclusions: Due to its superior classification accuracy, speed, and scalability to large datasets, ML-DSP is highly
relevant in the classification of newly discovered organisms, in distinguishing genomic signatures and identifying their
mechanistic determinants, and in evaluating genome integrity." <br> 
<br>
Keywords: Taxonomic classification, Whole genome analysis, Genomic signature, Alignment-free sequence analysis,
Machine learning, Numerical representation of DNA sequences, Digital signal processing, Discrete Fourier transform. <br>
*Correspondence: grandha8@uwo.ca
1Department of Computer Science, University of Western Ontario, London,
ON, Canada
Full list of author information is available at the end of the article

**DATASET**

Dataset used in this study are from NCIB and they are available in the following Gurjit S. Randhawa GitHub repositories: 
        
We will test our approach with 2 datasets: <br> 
        
        (1) Birds-Fish-Mammals    (553,)  Fishes:  (874,)  Mammals:  (2313,)
        
| Class   | Genomes     |  DNA sequence    |    
| ---     | ---         | ---              |
|         | (count)     |  (min-max length) |
| Birds   |   553       | ML Classification  |
| Fish    | 874         |  ML Classification |
| Mammals | 2313        |  ML Classification |       
        
https://github.com/grandhawa/MLDSP/tree/master/DataBase/Birds-Fish-Mammals
        
        (2) Fungis: Basidiomycota (only 30 genomes), Pezizomycotina, Saccharomycotina
        
https://github.com/grandhawa/MLDSP/tree/master/DataBase/Fungi


**OUR METHODOLOGY**

Birds - Fishes - Mammals
In this dataset, the authors achieve a 100% accuracy !         
We select the first NFFT=256, compute the FFT spectrum, we keep the phase. And without any particular pre-processing we achieve a 98-99% accuracy with Logistic Regression and SVM. After optimising hypermparameters.  <br>    
        
The method is inefficient when classifying fungis in three phylums:  . Unfortunately we had to introduce an alignement method for selecting optimal frames (lenght 256 points) before computiong the FFT.  At least in a first phase of this project we rely on "soft" alignement for selecting optimal frame, and achieveing a **94%** acuracy with SVM and rbf kernel. After optimizing hyperparameters. Which is better than the best result achived by the authors. The main drawback of our method is a very process of alignement presented in.  
        
        
In a third part, we will investigate a more complex numerical representation of DNA seuqnces for improved classification. Without the time consuming aligement technique.          
        
        
        
        

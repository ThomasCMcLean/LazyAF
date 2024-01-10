# LazyAF Pipeline

This pipeline is currently designed to work with [ColabFold_BATCH](https://github.com/sokrypton/ColabFold) for high-throughput protein structure and complex prediction. I wanted to create an accessible way of taking genome fasta files from [NCBI](https://www.ncbi.nlm.nih.gov/) and quickly adding on a bait protein sequence to each coding sequence, perform large scale in silico pulldown predictions and create a table of results to analyse. This all happens through Google Dive and Colaboratory.

This pipeline consist of three parts: 

[Part 1](https://colab.research.google.com/drive/1a5d7xraEK4Iv3Ecmmjb1opnU5jwXRW_a) produces individual fasta files for each coding sequence in the genome which have been modified to include the bait protein sequence as a second chain.

Part 2: You then can direct [AlphaFold2_BATCH](https://github.com/sokrypton/ColabFold) to this same results folder to directly perform the modelling and predictions.

[Part 3](https://colab.research.google.com/drive/1j7WJLcUHTR8BrjkWDaU549rFk6X5Zu18) then takes the raw output from these predictions and copies the rank_001 JSON files into a new folder before extracting the pTM and ipTM scores, calculating a Ranking_confidence score and putting that all into a .csv table for analysis.

For details, refer to our manuscript: in prep

N.B. I am wetlab scientist who has little experience in writing code. I am sure it can be streamlined and adapted for more than 2 protein interactions, or to accept fastas without [gene=] or [protein_id=] identifiers but currently I have not been able to achieve this smoothly.

Any issues, queries or comments please contact the corresponding author of the manuscript.

Thank you,
Tom

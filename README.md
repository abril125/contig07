METHODS:
1. BLAST (https://blast.ncbi.nlm.nih.gov/Blast.cgi)
In order to identify the species of the sequence given to us at the beginning (contigo7), we use blat and select the one with the highest percent identity and e value. In our case, the species is Caenorhabditis dougherty.

2. Ab-initio and homology-based methods
- We use GeneID and FGENESH to do the gene predictions (GENESCAN doesn't because it is not as good and specific as we expect). And we run them on both servers providing the contig07.fa file.
- We compare the areas when the exons start and finish and we see that the gene 1 of the FGENESH and the gene 2 of GeneID are very similar so we will do the alignment with these two.
- In the GeneID result, to obtain the sequence, we save the information of gene two in a GFF file and execute bedtools.
- Next, we wanted to run the two sequences obtained with our query, contigo07, in T-coffee to make the alignment, but the sequence of contigo07 (even removing the introns) was too long and did not allow us to enter it in T-coffee. Even so, knowing that the gene chosen for comparison is at the top of the contigo07 sequence, we trimmed the end of it a bit to be able to make the alignment.

3. Homology-based methods
- To contrast the results obtained in the ab-into methods, we use the exonerate.
- First, we use the blastx to download space with more similar matches with our query sequence.
- We run the exonerate and obtain a GFF file with the prediction of the exonerate to then be able to obtain a sequence with which to make the alignment in T-coffee in order to later be able to contrast with the results of the previous alignment.

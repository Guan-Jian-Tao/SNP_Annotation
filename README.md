#SNP Annotation
Method 1: <br>
>ANNOVA<br>
>Make Database using gtf file and genome fasta file.<br>
>Commoands:<br>
>gzip -c Bdistachyon_314_v3.0.clean.fa > Bdistachyon_314_v3.0.clean.fa.gz <br>
>gzip -c Bdistachyon_314_v3.1.gene_exons.clean.gtf > Bdistachyon_314_v3.1.gene_exons.clean.gtf.gz <br>
>gtfToGenePred -genePredExt Bdistachyon_314_v3.1.gene_exons.clean.gtf.gz BD_refGene.txt<br>
>perl retrieve_seq_from_fasta.pl --format refGene --seqfile Bdistachyon_314_v3.0.clean.fa BD_refGene.txt --out BD_refGeneMrna.fa <br>
>Now you can annotate a given VCF file. Please note that the --buildver argument should be set to BD. <br>
 




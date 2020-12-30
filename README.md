# AMPfinder <sub> V.1.0.2</sub>


To provide more opportunities for clinical solutions, we were thus motivated to design a homology-based gene prediction program (AMPfinder), an integrated tool stream that combines ORF prediction, and AMP classification to extract AMPs directly from genome or proteome sequence data.

  1.AMPfinder is a simple, yet accurate, computational pipeline that processes either genomes and proteome sequences. The search for AMPs is based on alignment searching the existing antimicrobial peptide database and predicting on the feature model in amino acid sequence obtained from the translation of the original transcriptome sequence data. The workflow showed as Figure.
  2.AMPfinder is a free software tool that combines ORF prediction and accurately classification of the AMPs from protein or nucleotide data, which performs translation of the input transcriptome data by using Prodigal, and selects short sequences containing ORF and signal peptide cleavage sites. Then, by default, DIAMOND was default used for homology detection and machine learning prediction model were used to search for potential AMPs, in which case all known or potential motifs will be revealed and classified. Due to the combination of various search methods, AMPfinder searcher allows to obtain the most complete repertoire of AMPs for one or more transcriptomes in a short amount of time. Therefore, AMPfinder seems to be the most suitable tool for rapid screening of potential AMPs.


USAGE:

python ampfinder main -i {INPUT_SEQUENCE} -o {OUTPUT_FILE} -t{contig,protein} -a{DIAMOND,BLAST} 



           -i INPUT_SEQUENCE,    --input_sequence INPUT_SEQUENCE
                        input file must be in FASTA (contig and protein) ! e.g myFile.fasta                       
           -o OUTPUT_FILE, 	    --output_file OUTPUT_FILE 
                        output folder and base filename      
           -t {contig,protein},	--input_type {contig,protein}
                        specify data input type (default = contig)
           -a {DIAMOND,BLAST},   --alignment_tool {DIAMOND,BLAST}
                        specify alignment tool (default = BLAST)
                        

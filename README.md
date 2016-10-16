# perch

PERCH is a software suite for the interpretation of rare or common genetic variants, including SNVs, InDels, structural variations, and de novo mutations. It evaluates the deleteriousness of variants, ranks genes for candidate selection, classifies variants as pathogenic or benign to a disease. It is useful for both gene discovery research and clinical genetic testing.

# Features

1. Broad integration: This framework has a broad integration of heterogeneous information, including deleteriousness, allele frequency, quality of variant calls from next generation sequencing (NGS), co-segregation of rare alleles with the disease within pedigrees, association of rare alleles with the disease among case-control samples, structural variations, de novo mutations in trios, the biological relevance of a gene to the disease of interest, gene expression profile, and previous study results.
2. Quantitative: All components are quantitatively integrated, without transforming a continuous value into a categorical score, or filtering variants by a threshold. This increases the power of the analysis and decreases the level of arbitrariness.
3. Flexible usage: Components of this framework can be assembled in various ways to accommodate different study designs or analysis aims. It is also easy to replace a component with another software, such as SEQlinkage for co­segregation analysis.
4. Whole genome: It works for whole genome sequencing, as well as whole exome sequencing or targeted sequencing data.
5. Function-aware: The deleteriousness score has taken into account the functional consequence of a variant to the protein sequence, such as splice-altering, frameshift, stop-gain, stop-loss, missense.
6. Liability classes and covariates: The segregation analysis can include liability classes. The rare­variant association analysis can include covariates.
7. Complex diseases: It was designed for complex disease research targeting rare or low­ frequency variants conferring a high or medium risk. It is powerful for complex traits as well as Mendelian and undiagnosed diseases.
8. Variant classification: This framework can do variant classification following the IARC (International Agency for Research on Cancer) guidelines for clinical genetic testing.
9. Unbiased benchmarking: The deleteriousness algorithm was appraised by carefully selected data set to avoid the type I, type II, and type III circularity.
10. Privacy: You can download programs and analyze your data locally. No information will be collected, stored, or sent out from your computer.

# Installation

Make sure your computer has the supported CPU architecture (X86_64), operating system (Linux with kernel 2.6.18 or later, Mac OS 10.7 or later), and the curl program. The disk space requirement for installation is about 4 GB.

Run one of the following commands to install the software. It doesn’t matter in which directory you run the command.

  example 1: install to your home folder in a computer cluster 
  curl -sL http://www.bjfenglab.org/download/victor.sh | bash

  example 2: install to your home folder in a Macbook Pro
  curl -sL http://www.bjfenglab.org/download/victor.sh | sudo bash

  example 3: install to a computer cluster for multiple research groups
  curl -sL http://www.bjfenglab.org/download/victor.sh | sudo PREFIX=/opt/local PROFILE=/etc/profile bash

Explanations: The default install directory is ~/local, which can be customized by PREFIX=/path/to/dir. The command will create a folder named “VICTOR” inside the install directory, then download and put files in it. After that, it will add “/path/to/dir/VICTOR” to $PATH in the ~/.profile (Mac OS) or ~/.bash_profile (Linux). The name of the PROFILE file can be customized by PROFILE=filename. Sometimes you may not have the privilege to write to the PROFILE file. In that case, please add “sudo” as in the second example. If you don’t want to add or remove $PATH, set “PROFILE=none”.

If it is the first time you install this software, please execute “source /path/to/PROFILE_file”, or log out and back in. This will reload the $PATH environment variable.

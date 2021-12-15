## Computing accuracy of imputation
#### Accepted imputed data format to compute imputation accuracy varies 
- Dosages (Genotype codes ranging from 0-2)
- Gene content (Discrete genotypes coded as 0, 1, 2) 
- Allele format (mostly in linkage and transposed linkage formats eg. PLINK PED and TPED)
---
#### Imputation accuracy is computed using four methods 
- Correlation between imputed and true genotypes
- Allelic correct rate (1 - allelic error rate)
- Percentage of correct calls
- Correlation between centered-imputed and centered-true genotypes (see Calus et al. 2014) 
---
#### The following arguments needed as an input file for the *"calc.imp.accuracy"* function in *"calc_imp_accu.R"* script  
- **truegeno**: Filename of true genotype (PLINK or allele dosage or gene content format)
- **imputedgeno**: Filename of imputed genotype (PLINK or allele dosage or gene content format)
- **mapHD**: Filename of the HIGH density SNP map file
- **mapLD**: Filename of the LOW density or imputed genotype SNP map file
- **nIID**: Number of animals genotyped, you can specify higher number but not less
- **format**: The format of the genotype data (either PLINK or gene content/allele dosage format)
- **accuracy_type**: The method to use in calculating accuracy (1. simple 2. calus_mulder 3. both)
- **missgeno**: The value of the missing genotype in the data file (eg. NA, 5, -9) 

**Note**: Both **imputedgeno and truegeno** arguements should have the same file format.

**Read**: *Evaluation of measures of correctness of genotype imputation in the context of genomic prediction: a review of livestock applications* (Calus et al. 2014 - http://dx.doi.org/10.1017/S1751731114001803 )



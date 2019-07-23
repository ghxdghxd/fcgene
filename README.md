# fcGENE

This repository is copied from <https://sourceforge.net/projects/fcgene/reviews>,
and fixs the bug in the fcGENE(1.0.7) for formating conversion of impute-imputed data.

## the bug

* impute.gen

```text
SNP_A-1909444 rs3094315 752566 G A 0 1 0 0 0 1 0 1 0
```

* impute.gen_info

```text
snp_id rs_id position a0 a1 exp_freq_a1 info certainty type info_type0 concord_type0 r2_type0
SNP_A-1909444 rs3094315 752566 G A 0.802 1.000 1.000 2 0.879 0.894 0.700
```

the bug: **the command option(--info-thresh) filters exp_freq_a1 instead of info in the impute.gen_info**

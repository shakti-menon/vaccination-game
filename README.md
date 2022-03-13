# Epidemic prevalence information on social networks can mediate emergent collective outcomes in voluntary vaccine schemes

[![Paper DOI : https://doi.org/10.1371/journal.pcbi.1006977](https://badgen.net/badge/PLOS%20Comput%20Bio%20DOI/10.1371%2Fjournal.pcbi.1006977)](https://doi.org/10.1371/journal.pcbi.1006977)

This repository contains data for Figures 2-4 of the manuscript:

> Sharma A, Menon SN, Sasidevan V and Sinha S (2019) Epidemic prevalence information on social networks can mediate emergent collective outcomes in voluntary vaccine schemes. _PLoS Comput Biol_ <b>15</b>(5): e1006977. 
> https://doi.org/10.1371/journal.pcbi.1006977

The data is in the form of ```.mat``` files (which can be opened in MATLAB).

*Note*: Data for the empirical social networks used in Figures 2(a-b) and 3(d) are openly accessible as part of the published article: 
Banerjee A, Chandrasekhar AG, Duflo E and Jackson MO (2013) The diffusion of microfinance. _Science_ <b>341</b>(6144): 1236498 https://doi.org/10.1126/science.1236498 
and can be directly downloaded from the Harvard Dataverse Repository [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=hdl:1902.1/21538).

The following table provides a description of the variables saved in the data files:

| Variable | Description |
| --- | --- |
| t | time instant |
| S(t) | the number of susceptible agents at time t |
| I(t) | the number of infected agents at time t |
| R(t) | the number of recovered agents at time t |
| V(t) | the number of vaccinated agents at time t |
| I<sub>c</sub>(t) | the cumulative number of infected agents at time t |
| inf<sub>&infin;</sub> | final fraction of infected agents |
| vac<sub>&infin;</sub> | final fraction of vaccinated agents |


## Contents of folder **Figure_2**

1. ```TimeSeries_Vill55_alpha0.mat```: Data for Fig. 2(a) and the left panel of Fig. 2(c)

This file contains a matrix ```S_rec``` of dimensions 692x6 that stores time series data for a single simulation on village network #55 for the case &alpha; = 0. The 6 columns correspond to: t, S(t), I(t), R(t), V(t) and I<sub>c</sub>(t).

2. ```TimeSeries_Vill55_alpha1.mat```: Data for Fig. 2(b) and the right panel of Fig. 2(c)

This file contains a matrix ```S_rec``` of dimensions 924x6 that stores time series data for a single simulation on village network #55 for the case &alpha; = 1. The 6 columns correspond to: t, S(t), I(t), R(t), V(t) and I<sub>c</sub>(t).

3. Subfolder ```vill55_network```: Data for Fig. 2(d) and Fig. 2(e)

This folder contains files for simulations on village network #55 for the cases &alpha; = 0 and &alpha; = 1. The file names are ```vill55_qX_alphaY.mat``` where X is the value of &beta; and Y is the value of &alpha; (0 or 1). Each ```.mat``` file contains a matrix ```datavn``` of dimensions 2x1000 that contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs.

## Contents of folder **Figure_3**

1. ```TimeSeries_ER_alpha0.mat```: Data for the left panel of Fig. 3(a)

This file contains a matrix ```S_rec``` of dimensions 885x6 that stores time series data for a single simulation on an Erd&#337;s-R&eacute;nyi network of size 1024 for the case &alpha; = 0. The 6 columns correspond to: t, S(t), I(t), R(t), V(t) and I<sub>c</sub>(t).

2. ```TimeSeries_ER_alpha1.mat```: Data for the right panel of Fig. 3(a)

This file contains a matrix ```S_rec``` of dimensions 1103x6 that stores time series data for a single simulation on an Erd&#337;s-R&eacute;nyi network of size 1024 for the case &alpha; = 1. The 6 columns correspond to: t, S(t), I(t), R(t), V(t) and I<sub>c</sub>(t).

3. Subfolder ```ER_network```: Data for Fig. 3(b) and Fig. 3(c)

This folder contains files for simulations on Erd&#337;s-R&eacute;nyi networks of size 1024 for the case of local information (&alpha; = 0, ```loc_*.mat```) and global information (&alpha; = 1, ```glo_*.mat```). The file names are ```X_glsp_qY.mat```, where X is "loc" or "glo" and Y is the value of &beta;. Each ```.mat``` file contains a matrix ```dataq``` of dimensions 2x1000 that contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs.

4. Subfolder ```Kavg_ERN_KVN```: Data for Fig. 3(d)

This folder contains files for simulations on Erd&#337;s-R&eacute;nyi networks of size 1024 as well as on empirical village networks.

For the case of Erd&#337;s-R&eacute;nyi networks, the file names are ```glsp_qX_kY_alphaZ.mat```, where X is the value of &beta;, Y is the average degree of the network used and Z is the value of &alpha; (0 or 1). Each ```.mat``` file contains a matrix ```dataq``` of dimensions 2x1000. This contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs.

For the case of village networks, the file names are ```villX_qY_alphaZ.mat```, where X is the village id, Y is the value of &beta; and Z is the value of &alpha; (0 or 1). Each ```.mat``` file contains a matrix ```datavn``` of dimensions 2x1000 that contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs.

## Contents of folder **Figure_4**

1. Subfolder ```ER_All_system_sizes```: Data for Fig. 4(a)

This folder contains simulations on Erd&#337;s-R&eacute;nyi networks for a range of system sizes (multiples of 1024), for the case of local and global information. The file names are ```Xn_alphaY_qZ.mat```, where X is the multiple of 1024 that specifies the system size (e.g. X="02" corresponds to a network of size 2\*1024=2048), Y is the value of &alpha; (0 or 1) and Z is the value of &beta;. Each ```.mat``` file contains a matrix ```dataq``` of dimensions 2x1000 that contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs.

2. Subfolder ```ER_16N```: Data for Fig. 4(b) and Fig. 4(c)

This folder contains simulations on Erd&#337;s-R&eacute;nyi networks for a fixed system size (16\*1024=16384 agents) and over a range of values of &alpha;. The file names are ```16n_alphaX_qY.mat```, where X is the value of &alpha; (0 or 1) and Y is the value of &beta;. Each ```.mat``` file contains a matrix ```dataq``` of dimensions 2x1000 that contains data for inf<sub>&infin;</sub> and vac<sub>&infin;</sub> over 1000 simulation runs. An additional 1000 simulation runs are provided in the files ```16n2_alphaX_qY.mat```, where X is the value of &alpha; (0 or 1) and Y is the value of &beta;.

A $Dst$-based space weather conditions machine learning classification model for GNSS PNT performance analysis

Ambient conditions classification enables systematic mitigation of adversarial effects on Global Navigation Satellite System (GNSS) Positioning, Navigation, and Timing (PNT) performance. This research contributes to the problem by proposing a classification model of space weather events for sub-equatorial regions. The proposed model uses machine learning-based classification applied to the experimental observations of geomagnetic field components, observed Total Electron Content ($TEC$), and Disturbance Storm-Time ($Dst$-index). A Support Vector Machine (SVM) with a Polynomial Kernel, C5.0 Decision Tree (DT), Naive Bayes (NB), shallow Neural Network (NN), Partial Least Squares (PLS), Flexible Discriminant Analysis (FDA), and shallow NN using Principal Component Analysis (PCA) was applied to develop the candidate model to classify observations of the geomagnetic field in $TEC$, combined with other variables, into one of the scenarios of space weather conditions. Performance is assessed using a confusion matrix and development time to yield the NB as the best performer. The proposed $Dst$-based classification model serves as an indicator of a geomagnetic/ionospheric storm in progress, thus alerting GNSS users of potential degradation in GNSS PNT performance and setting up a framework for the development of a tailored GNSS ionospheric correction model for specific classes of the space weather conditions.

The experiment was run on $Windows$ 11 using $R Studio$ version 2024.04.2+764 and $R$ version 4.4.1, the AMD Radeon RX 6600 Graphics Processing Unit (GPU), $16$ GB of Random Access Memory (RAM), and the AMD Ryzen 5 PRO 4650G Central Processing Unit (CPU) with $6$ cores. 

The annual observed $TEC$ data at Darwin, NT is contained in the file $darwin2014.csv$. The $TEC$ data set was derived from RINEX GPS observations using GPS $TEC$ software by Seemala.

The annual estimated $Dst$ and $a_{p}$ data in $2014$ is contained in the file $Dstap2014.dat$. The $Dst$ and $a_{p}$ data were derived from the INTERMAGNET data set, available from the INTERMAGNET website, and reformatted.

Model training can be run using the $ldtr2024\\_train.R$ script that automatically sets the working directory to the script's location on disk.

The script $ldtr2024\\_vars\\_analyze.R$ was used for the statistical analysis of input variable correlation and normal distribution.

The Python script $stat\\_test.py$ is used to run McNemar's test on the results.

The Python script $read\\_stat\\_test\\_and\\_distr.py$ and $read\\_txt\\_as\\_csv.py$ reformat the results for readability in $.txt$, $.csv$, and $.tex$ format.

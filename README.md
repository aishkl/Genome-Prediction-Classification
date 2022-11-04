# Genomics Classification & Prediction

The gene dataset : 23,000 feature columns (genes) and a target variable and 51 records .

Implemented an prediction model that predicts the set of final gene signature with high prediction accuracy.
For classification , the records (rows) having positive target variable into  are converted into “HS” and records having negative target variable into “HR”

Used feature selection techniques/dimensionality reduction/regularization to identify and reduce 
the features that are important for the prediction . The aim is to derive gene signatures that is small in number (<200 genes) and 
able to predict the target variable with high accuracy. 


The repository has 2 notebooks 

1) Gene_Classification -> For gene set classification
   - Applied PCA for feature dimension reduction
   - Selected number of dimensions required to preserve maximum variance : 38
   - Output of applying PCA with Logistic Regression :
      Test accuracy: 0.54
      Precision: 0.57
      Recall: 0.66
  - Experimented for best classifier : Out of which AdaBoostClassifier gave best results among other classifiers with 0.55% accuracy.
  - Experimenting with Feature selection using SelectKBest to select Top 200 features:
   List of Top 200 features:  ['AK5', 'MCOLN2', 'GBP5', 'LINC00622', 'TXNIP', 'S100A4', 'IFI16', 'FAM129A', 'SYT14', 'ID2', 'TRIB2', 'CDC42EP3', 'CYP1B1', 'CNRIP1',      'DGUOK.AS1', 'EVA1A', 'MALL', 'INHBB', 'TNFAIP6', 'PLA2R1', 'FAP', 'LINC01116', 'ITGA4', 'NRP2', 'C3orf14', 'GXYLT2', 'EPHA3', 'ARHGAP31', 'ROPN1', 'ROPN1B', 'TM4SF4', 'RARRES1', 'TRIM59', 'BCHE', 'TNFSF10', 'NLGN1', 'GNB4', 'CLDN1', 'PPP2R2C', 'S100P', 'SLIT2', 'SLC34A2', 'IGFBP7', 'CXCL8', 'EREG', 'AREG', 'ART3', 'PLAC8', 'SPP1', 'LEF1', 'ENPEP', 'PCDH18', 'LOC100507639', 'TRIM2', 'GK3P', 'GPM6A', 'SORBS2', 'FST', 'LUCAT1', 'MCTP1', 'PDLIM4', 'CD74', 'SPARC', 'HTATSF1P2', 'NRN1', 'DSP', 'GCNT2', 'RNF182', 'HLA.DPA1', 'LGSN', 'KCNQ5', 'POPDC3', 'FABP7', 'CTGF', 'EYA4', 'PLAGL1', 'SLC22A3', 'LOC100128885', 'PON3', 'DOCK4', 'AASS', 'AKR1B10', 'PTN', 'DLC1', 'SFRP1', 'PLAT', 'SNAI2', 'ZFHX4.AS1', 'MMP16', 'NIPAL2', 'COLEC10', 'HAS2', 'FBXO32', 'MTSS1', 'LINGO2', 'SNX18P3', 'ALDH1A1', 'DAPK1', 'PTGR1', 'TNC', 'PTGES', 'RNU5D.2P', 'OLFM1', 'AKR1C1', 'AKR1C5P', 'AKR1C3', 'LINC00842', 'HNRNPA1P33', 'AKR1B10P1', 'GSTO2', 'IFITM2', 'IFITM1', 'CDKN1C', 'AMPD3', 'LOC100129473', 'MYRF', 'FGF19', 'SYTL2', 'GRAMD1B', 'SLC6A13', 'C1S', 'GPRC5A', 'PLBD1', 'FAR2', 'TMTC1', 'SLC16A7', 'LYZ', 'TRHDE', 'CSRP2', 'ACSS3', 'SLC6A15', 'ALDH2', 'SLC46A3', 'CCNA1', 'LCP1', 'KCTD12', 'DCT', 'SLC7A7', 'LINC00520', 'GPX2', 'NEK9', 'IFI27', 'C14orf132', 'CRIP1', 'GABRB3', 'MIR626', 'C15orf48', 'SLC27A2', 'CA12', 'NEO1', 'CIB2', 'DNAJA4', 'TMC5', 'FRG2DP', 'CALB2', 'FAM101B', 'HS3ST3A1', 'CENPV', 'IGFBP4', 'TNS4', 'KRT20', 'KRT23', 'KANSL1.AS1', 'CDH2', 'RNF152', 'CFD', 'UCA1', 'ZFP82', 'LOC284412', 'CEACAM6', 'APOC1', 'LOC645553', 'PLTP', 'BAGE2', 'CXADR', 'TMPRSS15', 'TIMP3', 'LOC441528', 'GPR143', 'GPM6B', 'IL1RAPL1', 'TMEM47', 'SYTL5', 'SRPX', 'SLC38A5', 'ARMCX1', 'ZMAT1', 'BEX1', 'TCEAL3', 'IL13RA2', 'KLHL13', 'TENM1', 'GPC3', 'FGF13', 'GABRA3', 'MAGEA6', 'MAGEA12', 'PNMA6A', 'RPS4Y1', 'CD24']
   
   
3) Gene_Prediction ->  For gene set prediction
 - Used LASSO for feature selection which picked 135 variables giving best prediction with R2 Error of 0.018
 - Output for final gene signature :
      LINC00337       0.026094
      LOC100132942    0.063610
      PLA2G2C         0.156274
      MUL1           -0.008242
      PFN1P10        -0.024065
                  ...   
      IGLV3.25       -0.011779
      TYMP            0.000367
      PPP4R3CP       -0.000380
      CXorf21         0.017118
      LOC100287728    0.011754




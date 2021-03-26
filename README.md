# Introduction
This repository contains the information used in pre-processing of the MS/MS spectra and how this can be used to improve the identification of non-human peptides from the raw files.

## Experimental procedure
- [x] Remove low quality and spectra that are unassigned/ non-informative. The non-informative spectra were removed by use of pClean bioconductor tool
- ![image](https://user-images.githubusercontent.com/26459707/112679481-e2f52800-8e74-11eb-8193-297cf585883b.png)
> Filtering the MS/MS to increase signal to noise ration (S/N)
- [x] Identify human peptides (proteins from the classical analysis)
- [x] Identify non-human peptides (proteins)
- [x] Carry out open modification search (Including both human and non-human protein peptides)
- [x] Identify non-peptide compounds (metabolites) from singuly charged spectra
- [x] Re-callibrate the overall assignment rate based on the sum of the above, relative to the total number of high quality non-redudant spectra.
- [x] The clearance of uninformative MS/MS signals was done using pClean [tool](https://pubs.acs.org/doi/pdf/10.1021/acs.jproteome.9b00141?rand=ztz0p6rs). This was done to remove the low quality and redudant spectra from the RAW files prior to the standard database search.
-------------------------------------------------------------------------------------------------------------------------------------
## Identification of human and non-human peptides
This was done using the MSfragger version (V 3.1.1)
![figure_1](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/cleanedUncleanedMetaNovocleaned%20search%20pct.png)
> Figure 1: Venn diagram showing the protein identifications overlaps from the standard uncleaned spectra, the pCleaned specral data and the cleaned data search against sample specific database. The identification overlap is shown in percentage.

![Figure_2](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/cleanedmetauncleaned.png)
> Figure 2: Venn diagram showing the protein identifications overlaps from the standard uncleaned spectra, the pCleaned specral data and the cleaned data search against sample specific database. The identification overlap is shown in absolute values.

![Figure_3](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/metaStandardSpectraabs.png)
> Figure 3: Venn diagram showing the protein identifications overlap between uncleaned spectra, pCleaned spectra and the sample specific database seach against the standard uncleaned spectra in absolute values.

![Figure_4](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/metanovouncleanedSpectra.png)
> Fifure 4: Venn diagram showing the protein identifications overlap between uncleaned spectra, pCleaned spectra and the sample specific database seach against the standard uncleaned spectra in percentages.
----------------------------------------------------------------------
![Figure_5](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/nonHumanproteinsoverlaps.png)
> Figure 5: Non-human protein overlaps between pCleaned and uncleaned spectra using sample specific database generated by MetaNovo.

------------------------------------------------------------------
![Figure_6](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/pclean_AND_metcomparison.png)
> Figure 6: pClean and MetaNovo comparison

----------------------------------------------------------------
![Figure_7](https://github.com/javanOkendo/spectralProcessing/blob/main/Figures/pcleanvsstandardSearch.png)
> Figure 7: pCleaned vs standard spectral searches using the standard human database
-----------------------------------------------------------------------------------------------------------------------------------------
## Open modification searching
- [x] This analysis is done to determine the potential post-translational modifications that could be present in our data.
- [x] We use MSfragger v 3.1.1 for the opem modification searches of the PTMs and the PTMprophet in determining the actual PTMs in our data.

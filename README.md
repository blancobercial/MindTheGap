# MindTheGap

<b>An Analytical Tool to Study the Barcoding Gap</b>

MindTheGap is a simple tool in java to study the barcode gap (Hebert et al., 2003; Hebert et al., 2004; Meyer and Paulay, 2005). The idea behind this tool is to target the gap itself. Instead of studying the distribution of the between-individuals distances in the dataset, MindTheGap finds the first gap based on a user-provided minimum length and returns the distribution of that gap on bins of a user-provided size.

It has been tested only in a Windows environment (XP and 7), but it should work independently of the operational system.

<b>How it Works</b>

The infile is a comma-delimited matrix of genetic (or any other kind of) distances like the one you can easily obtain from MEGA (Tamura et al., 2011) for example. Once you open the file, the number of individuals and comparisons should be indicated. The tool removes missing (any non-numeric) data from the analysis. Once you select the starting point of analysis (you may prefer to start analyzing above a certain threshold if your coverage of the diversity is low to avoid false positives), the minimum size of the gap to be considered and the bin size.

MindTheGap searches within the distances belonging to each individual for the first gap equal or larger than the minimum established, and when found, returns the extension of the gap in bin-size increments.

Once you have run it, the ROOT name for the outfiles has to be provided.

<b>The Output Files</b>

The output files from MTG include:

a) Four files: ROOT_SUMMARY.txt: this file describes the infile name, the number of individuals included, and the values for a starting point, minimum gap size and bin size. Furthermore, it indicates the name of the other four files and a brief description of what they include. ROOT1.txt includes the distribution of the gap for each individual, as a comma-delimited table. ROOT2.txt provides the minimum, the maximum, the average, and the extension of the gap. Finally, ROOT3.txt will recover those individuals that showed no gap under the established conditions (if all showed the gap, the file would indicate “NONE”). Our idea with these outfiles was to provide outfiles that were easy-to-adapt to any other software (for example, excel and equivalents, MATLAB or R) to continue your analysis.

<b>Disclaimer</b>

This tool is provided “as is”, for use in Research and Education. This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. This program is distributed in the hope that it will be useful, but without any warranty; without even the implied warranty of merchantability or fitness for a particular purpose.  See the GNU General Public License for more details.

<b>References</b>

Hebert, P. D., Cywinska, A., Ball, S. L. and Dewaard, J. R. (2003) Biological identifications through DNA barcodes. Proc. R. Soc. B: Biol. Sci., 270, 313 - 321.
Hebert, P. D., Stoeckle, M. Y., Zemlak, T. S. and Francis, C. M. (2004) Identification of birds through DNA barcodes. PLoS Biol., 2, E312.
Meyer, C. P. and Paulay, G. (2005) DNA Barcoding: error rates based on comprehensive sampling. PLoS Biol., 3, e422.
Tamura, K., Peterson, D., Peterson, N., Stecher, G., Nei, M., Kumar, S., 2011. MEGA5: Molecular Evolutionary Genetics Analysis using maximum likelihood, evolutionary distance, and maximum parsimony methods. Mol. Biol. Evol. 28, 2731-2739.

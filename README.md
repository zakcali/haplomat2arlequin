# haplomat2harlequin
convert HLA data format from Hapl-o-Mat to Arlequin

one can analyse HLA data with various software

Hapl-o-Mat can read various formats : https://github.com/DKMS/Hapl-o-Mat/tree/master/examplePopulations

if you entered your data into Hapl-o-Mat in MAC format, you can export your data to Arlequin format easly

download raw data containing 100 samples of HLA data from https://github.com/DKMS/Hapl-o-Mat/blob/master/examplePopulations/populationData_a.dat

save as populationData_a.dat.txt

convert2arlequin.html javascript program uses paparse.min.js to read csv files, extracts locus names from the first line of csv / or table delimited file

steps:

	1- run the program convert2arlequin.html
	2- click choose file and select populationData_a.dat.txt
	3- click read and see the MAC formatted file in CSV input / Arlequin Output
	4- click convert and see the arp formatted file in CSV input / Arlequin Output
	5- click copy
	6- paste to your favorite text editor (for example notepad++)
	7- save as from your favorite text editor, give a name with extension arp
	8- open arp file as a project from Arlequin

you can change the options below, such as 	RecessiveData before saving data:

[Profile] 

	Title="A sample of human HLA data with recessive alleles"

	NbSamples=1
	GenotypicData=1
	DataType=STANDARD
	RecessiveData=1
	GameticPhase=0
	RecessiveAllele="NULL"
	LocusSeparator=WHITESPACE
	MissingData="?"

[Data]

	[[Samples]]

		SampleName="A test HLA sample"
    

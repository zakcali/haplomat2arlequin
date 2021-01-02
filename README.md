# haplomat2arlequin
converts HLA data from Hapl-o-Mat to Arlequin.

It is not necessary to be on a server, because written in pure JavaScript. You can save html file to your computer, start it in a browser, by double clicking the html file. Your csv or tab-delimited files can be read from your hard disk.

Most people keep his/her HLA data on an Excel file, and examine them with various software. Hapl-o-mat and Arlequin are just two of them.

Hapl-o-Mat can read various formats : https://github.com/DKMS/Hapl-o-Mat/tree/master/examplePopulations

You can find more information about formats from page 11+ of https://github.com/DKMS/Hapl-o-Mat/blob/master/detailedGettingStartedWindows.pdf

MAC (Multiple Allele Codes) is one of those formats, and you can export from Excel if you keep your archive in Excel fomat


if you entered your data into Hapl-o-Mat in MAC format, you can convert your data to Arlequin format by using haplomat2arlequin

download raw data containing 100 samples of HLA data from https://github.com/DKMS/Hapl-o-Mat/blob/master/examplePopulations/populationData_a.dat

save as populationData_a.dat.txt

convert2arlequin.html javascript program uses paparse.min.js to read csv files, extracts locus names from the first line of comma seperated or table delimited file

steps:

	1- click to convert2arlequin.html to run in a browser 
	2- click choose file and select populationData_a.dat.txt
	3- click read and see the MAC formatted file in "CSV input / Arlequin Output" text area
	4- click convert and see the arp formatted file in "CSV input / Arlequin Output" text area
	5- click copy
	6- paste to your favorite text editor (for example notepad++)
	7- save as from your favorite text editor, give a name with extension arp
	8- open arp file as a project from Arlequin
	9- instead of (5-8) you can use save button if your browser is compatible

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
    

You can also use the haplomat2arlequin to read HLA data entered in Excel files

steps

	1- Your excel documents first row must contain an id column, followed by HLA domains twice
	2- Export your data as a csv file (it may contain commas instead of tabs, thanks to papaparse)
	3- read csv file from convert2arlequin.html, just like Hapl-o-Mat in MAC format

What:
You entered your data in excel, a line for every person. Arlequins wants one item for every HLA data. If more than one person shares same HLA data, you must supply:

	1- An arbitrary (group) name for HLA data
	2- Frequency of HLA data (how many person have that HLA data
	3- HLA data itself
If a HLA data is unique in the population, frequency must 1 

you can choose a prefix for group data by entering an arbitrary letter in Group prefix: before converting with convert2arlequin.html

If you look at last line-1 of Arlequin output  then you understand how many HLA groups is present in your population.

Output of sample csv file, can be seen HLA-people.arp
Hint: "2" after G1 means there are two people having this genotype

G1       2  A*03   B*31   C*04   DR*04   DQ*04   
            A*24   B*57   C*06   DR*07   DQ*03  

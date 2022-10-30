# pip install pathlib
# pip install PyPDF2
# pip install pandas
# pip3 install glob
# pip install openpyxl


#1.Merging PDF
from pathlib import Path
from PyPDF2 import PdfFileMerger, PdfFileReader

# Define input directory for the pdf files
pdf_dir = Path(__file__).parent / "RawData_PDF_Download"

#Define & create output directory
pdf_output_dir = Path(__file__).parent / "Company_Data"
pdf_output_dir.mkdir(parents=True, exist_ok=True) # Set exist_ok=True to prevent error in case the parent output folder already exist

#List all pdf files in the input directory
RawData_PDF_Download = list(pdf_dir.glob("*.pdf"))

#Merging approach
    #in this example: downloaded pdf name as "0123456789123.2020-01-31.Company Overview.pdf"
keys = set([file.name[:24] for file in RawData_Download_CorpusX])

for key in keys:
    merger = PdfFileMerger()
    for file in RawData_Download_CorpusX:
        if file.name.startswith(key):
            merger.append(PdfFileReader(str(file), "rb"))
    merger.write(str(pdf_output_dir / f"{key}.pdf"))
    merger.close()

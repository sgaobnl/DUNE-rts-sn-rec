Implementation of text recognition techniques for use in DUNE Cold Electronics, to read out serial numbers from LArASIC chips.
Chip pictures come from RTS at BNL.

1) "SN_tesserocr.py" performs OCR based on Python Tesseract (needs more work!)
2) "SN_chip_CPM.py" performs OCR based on OpenBMB MiniCPM-V-2_6 (https://huggingface.co/openbmb/MiniCPM-V-2_6). We will use this version for the SN recognition from now on (November 2024).
3) "produce_json.py" loops over all OCR results in "Tested/<TESTED_BATCH>/ocr_results" to produce the corresponding .JSON files that will be used to create records in HWDB.
4) "upload_LArASICs.py" will send such records to HWDB using a set of CURL commands.

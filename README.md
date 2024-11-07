# Exercise 13: Invoice Processing automation using OCR

### Reg No: 212221040013

## AIM:
To extract and save specific invoice details from a PDF using OCR in UiPath.

## Activities Required:
1. Read PDF with OCR
2. Matches
3. Excel Application Scope
4. Write Cell

## Procedure:
1. Create a new **InvoiceProcessing** project in UiPath Studio.
   
2. Add **Read PDF with OCR** activity to read the invoice PDF, set **FileName** to the PDF path, and select **Tesseract OCR** as the OCR engine.

3. Create **invoiceText** variable to store the OCR-extracted text.

4. Use **Matches** activity with **invoiceText** to extract specific data:
   - Invoice Number: `INV-\d+`
   - Date: `\d{2}/\d{2}/\d{4}`
   - Amount: `\$?\d+(,\d{3})*(\.\d{2})?`

5. Add **Excel Application Scope** and set **File Path** to save extracted data in Excel.

6. Use **Write Cell** activity to save:
   - Invoice Number in **A1**
   - Date in **A2**
   - Amount in **A3**

## Workflow:
![image](https://github.com/user-attachments/assets/c74dd8fb-f57d-4c17-b5c0-cbc9b8fe499f)

## Output:
![image](https://github.com/user-attachments/assets/a470aa03-d2a6-498b-a7d1-8e1fa9f24f27)

## Result:
The invoice details are successfully extracted from PDF and saved in Excel.

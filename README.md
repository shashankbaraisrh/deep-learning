# Invoice-to-HTML Processor using OCR and LLM

This project converts invoice images into structured HTML using **Tesseract OCR** for text extraction and an **LLM** for intelligent content analysis. It reconstructs invoice layouts while replacing dynamic content with placeholders, making it ideal for automated invoicing systems or document processing workflows.

---

## Features

* **OCR Text Extraction**: Extracts text with layout data from invoices.
* **Dynamic Content Detection**: Replaces names, emails, addresses, invoice numbers, amounts, etc., with placeholders (`@@Name@@`, `@@InvoiceNumber@@`, etc.).
* **Table Recognition**: Detects tables and recreates them in HTML while maintaining structure.
* **Layout Preservation**: Maintains the look and feel of the original invoice.
* **Anonymization**: Ensures safe sharing by replacing sensitive data with placeholders.

---

## How It Works

1. **OCR Extraction**: Tesseract extracts text and coordinates from the invoice.
2. **LLM Analysis**: The LLM identifies dynamic content and organizes the invoice into structured HTML.
3. **HTML Output**: Generates HTML with placeholders and inline CSS, preserving tables, text, and layout.

---

## Supported Placeholders

| Placeholder         | Description                 |
| ------------------- | --------------------------- |
| @@Name@@            | Customer or recipient name  |
| @@Email@@           | Email addresses             |
| @@Date@@            | Dates                       |
| @@PaymentMethod@@   | Payment method              |
| @@ID@@              | IDs or reference numbers    |
| @@Address@@         | Street, city, postal info   |
| @@Organization@@    | Company name                |
| @@PhoneNumber@@     | Contact numbers             |
| @@InvoiceNumber@@   | Invoice numbers             |
| @@Amount@@          | Payment amounts             |
| @@Tax@@             | Tax details                 |
| @@ItemDescription@@ | Product/service description |
| @@Quantity@@        | Quantity of items           |
| @@UnitPrice@@       | Price per unit              |
| @@TotalPrice@@      | Total amount for line items |

---

## Requirements

* Python 3.8+
* **pytesseract**: `pip install pytesseract`
* **Pillow**: `pip install pillow`
* **openai**: `pip install openai`
* **json**: Python standard library

---

## Workflow

1. Input invoice image (`.png`, `.jpg`, `.pdf`).
2. OCR extracts text and layout.
3. LLM analyzes content and generates HTML with placeholders.
4. Output: structured HTML ready for display or storage.

---

## Benefits

* **Automated Extraction**: Reduces manual errors.
* **Reusable Templates**: Placeholders allow dynamic use.
* **Accurate Layout**: Preserves tables and formatting.
* **Secure Sharing**: Sensitive data anonymized with placeholders.


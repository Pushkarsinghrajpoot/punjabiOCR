# Punjabi Translator

A Streamlit application designed to extract and translate Punjabi text from PDF documents to English, with specialized parsing for voter list documents.

## Features

- **PDF Text Extraction**: Uses OCR (Tesseract) to extract text from PDF files.
- **Punjabi to English Translation**: Translates extracted Punjabi text to English using Google Translate API.
- **Structured Data Parsing**: Parses translated text to extract polling station details and section information.
- **Tabular Output**: Formats results into a tabular structure with the following columns:
  - Polling Station Number
  - Building and Address
  - Sections Covered
- **Export Options**: Supports exporting translated data to text files or Excel spreadsheets.
- **Single and Batch Processing**: Process individual PDF files or multiple files in one go.

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/PunjabiTranslator.git
   cd PunjabiTranslator
   ```

2. Install required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Ensure Tesseract OCR is installed on your system:
   - Windows: Download from [https://github.com/UB-Mannheim/tesseract/wiki](https://github.com/UB-Mannheim/tesseract/wiki)
   - Linux: `sudo apt-get install tesseract-ocr`
   - Mac: `brew install tesseract`

## Usage

Run the Streamlit app:
```
streamlit run app.py
```

Then open your browser and navigate to the displayed URL (typically http://localhost:8501).

### Using the Application

1. **Upload PDF**: Use the file uploader to select a Punjabi PDF document.
2. **Process**: Click the "Process PDF" button to extract and translate the text.
3. **View Results**: Examine the structured output in the Streamlit interface.
4. **Export**: Download the results in your preferred format (text or Excel).

## Project Structure

- `app.py`: Main Streamlit interface
- `PunjabiTranslator/ocr_processor.py`: Handles OCR using Tesseract
- `PunjabiTranslator/pdf_handler.py`: Manages PDF file operations
- `PunjabiTranslator/translator.py`: Handles translation using Google Translate API

## Dependencies

- streamlit
- pandas
- googletrans
- pdf2image
- pytesseract
- Pillow
- openpyxl

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Google Translate API for translation services
- Tesseract OCR for text extraction from images
- Streamlit for the user interface

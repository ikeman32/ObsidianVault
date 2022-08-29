```Python
from pdf2docx import Converter

  

pdf_file = "./BookWritingGuide.pdf"

  

docx_file = "./BookWritingGuide.docx"

  

cv = Converter(pdf_file)

  

cv.convert(docx_file)

  

cv.close()
```

This Code does work but graphics, specifically graphics with text does not work correctly.
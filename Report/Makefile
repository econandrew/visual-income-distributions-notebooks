CHROME=/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome
PDFCAT="/System/Library/Automator/Combine PDF Pages.action/Contents/Resources/join.py"

pdf: html
	mkdir pdf; \
	for f in html/*.html; do \
		$(CHROME) --headless --disable-gpu --print-to-pdf=pdf/`basename $$f .html`.pdf file://`pwd`/$$f; \
	done; \
	$(PDFCAT) -o pdf/Report.pdf pdf/*.pdf

pdf2: *.ipynb
	mkdir pdf2; \
	nbmerge *.ipynb > Report.ipynb; \
	jupyter-nbconvert --to pdf --template=kcp_report.tplx Report.ipynb; \
	mv Report.pdf pdf2/; rm Report.ipynb

html: *.ipynb
	jupyter-nbconvert --output-dir=html --to html *.ipynb; \
	cp -R images html/

clean:
	rm -R html; \
	rm -R pdf; \
	rm -R pdf2

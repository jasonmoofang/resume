# This resume is meant to be put up on the web
# Should update from time to time with latest publications

BACKUP_DIR = /old_home/benleong/resume
HOME_DIR = clementi.mit.edu:/home/benleong/resume
REMOTE_DIR = telesto.lcs.mit.edu:/home/benleong/resume
PAPER = resume

all:	$(PAPER).tex
#	latex $(PAPER).tex
	pdflatex $(PAPER).tex

ps:	$(PAPER).tex
	latex $(PAPER).tex
	dvips -t a4 -o $(PAPER).ps $(PAPER)

v:	$(PAPER).pdf
	xpdf $(PAPER).pdf &

pdf: 	$(PAPER).ps
	ps2pdf $(PAPER).ps

backup: 
	cp * $(BACKUP_DIR)
	scp * $(REMOTE_DIR)

reverse: 
	scp * $(HOME_DIR)

clean:
	rm *.ps *.pdf $(PAPER).log $(PAPER).bbl $(PAPER).toc $(PAPER).blg $(PAPER).dvi $(PAPER).aux *~

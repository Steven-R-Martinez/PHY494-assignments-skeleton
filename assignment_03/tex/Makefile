YEAR  := 2020
NAME  := assignment_03
LATEX := $(NAME).tex
PDF   := $(NAME).pdf

SKELETON := $(HOME)/Documents/Teaching/ASU/CompPhys_PHY494/$(YEAR)/PHY494-assignments-skeleton/$(NAME)
SUBMISSION := $(SKELETON)/Submission
TEX := $(SKELETON)/tex

%.pdf: %.tex
	pdflatex -shell-escape $<
	pdflatex -shell-escape $<

.phony: all see copy

all: $(PDF)

see: $(PDF)
	open $^

copy: $(PDF)
	-mkdir -p $(SKELETON)
	-mkdir $(SUBMISSION) $(TEX)
	cp $^ $(SKELETON)
	cp code/*.py $(SUBMISSION)
	cp $(LATEX) Makefile $(TEX)



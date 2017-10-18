SRCDIR := ./
OUTDIR := ../_posts
TESTDIR := ./
SRCS := $(wildcard $(SRCDIR)/*.md)
OUT_FILES := $(addprefix $(OUTDIR)/, $(SRCS:.md=.html))
TEST_FILES := $(addprefix $(TESTDIR)/, $(SRCS:.md=.html))
TEMPLATE_DIR = ./templates

.SUFFIXES:	.md .html .epub .pdf
all: $(OUT_FILES)
$(OUTDIR)/%.html:%.md
	pandoc -f markdown+autolink_bare_uris  -t html --template=$(TEMPLATE_DIR)/template_jekyll --mathjax -o $@ $<

test: $(TEST_FILES)
$(TESTDIR)/%.html:%.md
	pandoc -f markdown+autolink_bare_uris  -t html --template=$(TEMPLATE_DIR)/template_katex --mathjax -o $@ $<

clean:
	rm *.html



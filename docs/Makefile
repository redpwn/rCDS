# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = .
BUILDDIR      = _build

SPHINXAUTOBUILD ?= sphinx-autobuild

.DEFAULT_GOAL = build

.PHONY: Makefile build livebuild

# Convenience target
build: dirhtml
	@

livebuild: livedirhtml
	@

live%: Makefile
	@$(SPHINXAUTOBUILD) -b $(subst live,,$@) "$(SOURCEDIR)" "$(BUILDDIR)/$(subst live,,$@)" $(SPHINXOPTS) $(O)

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

CLEANFILES = *~
MAINTAINERCLEANFILES = Makefile.in

AM_CXXFLAGS = -I$(top_srcdir) -std=c++14 -Wall -Wextra -pedantic

noinst_LIBRARIES = libcli.a

libcli_a_SOURCES = \
	cli_dumper.cc cli_dumper.hh \
	cli_error.cc cli_error.hh \
	cli_group.cc cli_group.hh \
	cli_handler.cc cli_handler.hh \
	cli_section.cc cli_section.hh \
	cli_option.cc cli_option.hh \
	cli_visitor.cc cli_visitor.hh

bin_PROGRAMS = \
	eos-evaluate \
	eos-list-constraints \
	eos-list-observables \
	eos-list-parameters \
	eos-list-signal-pdfs \
	eos-print-polynomial

LDADD = \
	$(top_builddir)/eos/statistics/libeosstatistics.la \
	$(top_builddir)/eos/utils/libeosutils.la \
	$(top_builddir)/eos/maths/libeosmaths.la \
	$(top_builddir)/eos/models/libeosmodels.la \
	$(top_builddir)/eos/form-factors/libeosformfactors.la \
	$(top_builddir)/eos/b-decays/libeosbdecays.la \
	$(top_builddir)/eos/rare-b-decays/libeosrarebdecays.la \
	$(top_builddir)/eos/meson-mixing/libeosmesonmixing.la \
	$(top_builddir)/eos/libeos.la \
	libcli.a \
	-lboost_filesystem -lboost_system \
	$(YAMLCPP_LDFLAGS)

eos_evaluate_SOURCES = eos-evaluate.cc

eos_list_constraints_SOURCES = eos-list-constraints.cc
eos_list_constraints_CXXFLAGS = $(AM_CXXFLAGS) $(YAMLCPP_CXXFLAGS)

eos_list_observables_SOURCES = eos-list-observables.cc

eos_list_parameters_SOURCES = eos-list-parameters.cc

eos_list_signal_pdfs_SOURCES = eos-list-signal-pdfs.cc

eos_print_polynomial_SOURCES = eos-print-polynomial.cc
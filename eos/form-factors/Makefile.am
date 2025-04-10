CLEANFILES = *~
MAINTAINERCLEANFILES = Makefile.in

AM_CXXFLAGS = @AM_CXXFLAGS@
AM_LDFLAGS = @AM_LDFLAGS@

lib_LTLIBRARIES = libeosformfactors.la
libeosformfactors_la_SOURCES = \
	analytic-b-to-pi.hh analytic-b-to-pi.cc \
	analytic-b-to-pi-pi.hh analytic-b-to-pi-pi.cc \
	analytic-b-to-p-lcsr.hh analytic-b-to-p-lcsr-impl.hh \
	analytic-b-to-pi-lcsr.cc  analytic-b-to-k-lcsr.cc  analytic-b-to-d-lcsr.cc \
	analytic-bs-to-k-lcsr.cc  analytic-bs-to-ds-lcsr.cc \
	analytic-b-to-v-lcsr.hh analytic-b-to-v-lcsr-impl.hh \
	analytic-bs-to-kstar-lcsr.cc analytic-bs-to-dsstar-lcsr.cc analytic-bs-to-phi-lcsr.cc \
	analytic-b-to-rho-lcsr.cc analytic-b-to-kstar-lcsr.cc analytic-b-to-dstar-lcsr.cc \
	baryonic.cc baryonic.hh baryonic-impl.hh \
	baryonic-processes.hh \
	b-lcdas.cc b-lcdas.hh \
	form-factor-adapter.hh \
	form-factors.cc form-factors.hh form-factors-fwd.hh \
	hqet-b-to-c.hh hqet-b-to-c.cc \
	kstar-lcdas.cc kstar-lcdas.hh \
	lcda.cc lcda.hh \
	mesonic.cc mesonic.hh mesonic-impl.hh \
	mesonic-hqet.hh \
	mesonic-processes.hh \
	observables.cc observables.hh \
	parametric-abr2022.hh parametric-abr2022-impl.hh parametric-abr2022.cc \
	parametric-bcl2008.hh parametric-bcl2008-impl.hh parametric-bcl2008.cc \
	parametric-bgl1997.hh parametric-bgl1997-impl.hh parametric-bgl1997.cc \
	parametric-bmrvd2022.hh parametric-bmrvd2022-impl.hh parametric-bmrvd2022.cc \
	parametric-bsz2015.hh parametric-bsz2015-impl.hh parametric-bsz2015.cc \
	parametric-kmpw2010.hh parametric-kmpw2010-impl.hh parametric-kmpw2010.cc \
	pi-lcdas.cc pi-lcdas.hh \
	unitarity-bounds.cc unitarity-bounds.hh \
	zero-recoil-sum-rule.cc zero-recoil-sum-rule.hh
libeosformfactors_la_CXXFLAGS = $(AM_CXXFLAGS) $(GSL_CXXFLAGS)
libeosformfactors_la_LDFLAGS = $(AM_LDFLAGS) $(GSL_LDFLAGS)
libeosformfactors_la_LIBADD = \
	$(top_builddir)/eos/utils/libeosutils.la \
	$(top_builddir)/eos/maths/libeosmaths.la \
	$(top_builddir)/eos/models/libeosmodels.la \
	-lgslcblas \
	-lgsl

include_eos_rarebdecaysdir = $(includedir)/eos/form-factors
include_eos_rarebdecays_HEADERS = \
	analytic-b-to-pi.hh \
	analytic-b-to-pi-pi.hh \
	b-lcdas.hh \
	form-factor-adapter.hh \
	form-factors.hh \
	observables.hh \
	parametric-abr2022.hh \
	parametric-bcl2008.hh \
	parametric-bgl1997.hh \
	parametric-bsz2015.hh \
	parametric-kmpw2010.hh \
	pi-lcdas.hh

AM_TESTS_ENVIRONMENT = \
	export EOS_TESTS_PARAMETERS="$(top_srcdir)/eos/parameters";

TESTS = \
	analytic-b-to-pi_TEST \
	analytic-b-to-pi-pi_TEST \
	analytic-b-to-p-lcsr_TEST \
	analytic-b-to-v-lcsr_TEST \
	baryonic_TEST \
	b-lcdas_TEST \
	hqet-b-to-c_TEST \
	kstar-lcdas_TEST \
	lcda_TEST \
	mesonic_TEST \
	mesonic-hqet_TEST \
	parametric-abr2022_TEST \
	parametric-bcl2008_TEST \
	parametric-bgl1997_TEST \
	parametric-bmrvd2022_TEST \
	parametric-bsz2015_TEST \
	parametric-kmpw2010_TEST \
	pi-lcdas_TEST \
	unitarity-bounds_TEST
LDADD = \
	$(top_builddir)/test/libeostest.la \
	libeosformfactors.la \
	$(top_builddir)/eos/models/libeosmodels.la \
	$(top_builddir)/eos/maths/libeosmaths.la \
	$(top_builddir)/eos/utils/libeosutils.la \
	$(top_builddir)/eos/libeos.la

check_PROGRAMS = $(TESTS)

analytic_b_to_pi_TEST_SOURCES = analytic-b-to-pi_TEST.cc

analytic_b_to_pi_pi_TEST_SOURCES = analytic-b-to-pi-pi_TEST.cc
analytic_b_to_pi_pi_TEST_CXXFLAGS = $(AM_CXXFLAGS) $(GSL_CXXFLAGS)

analytic_b_to_p_lcsr_TEST_SOURCES = analytic-b-to-p-lcsr_TEST.cc

analytic_b_to_v_lcsr_TEST_SOURCES = analytic-b-to-v-lcsr_TEST.cc

baryonic_TEST_SOURCES = baryonic_TEST.cc

b_lcdas_TEST_SOURCES = b-lcdas_TEST.cc

hqet_b_to_c_TEST_SOURCES = hqet-b-to-c_TEST.cc

kstar_lcdas_TEST_SOURCES = kstar-lcdas_TEST.cc

lcda_TEST_SOURCES = lcda_TEST.cc

mesonic_TEST_SOURCES = mesonic_TEST.cc

mesonic_hqet_TEST_SOURCES = mesonic-hqet_TEST.cc

parametric_abr2022_TEST_SOURCES = parametric-abr2022_TEST.cc

parametric_bcl2008_TEST_SOURCES = parametric-bcl2008_TEST.cc

parametric_bgl1997_TEST_SOURCES = parametric-bgl1997_TEST.cc

parametric_bsz2015_TEST_SOURCES = parametric-bsz2015_TEST.cc

parametric_bmrvd2022_TEST_SOURCES = parametric-bmrvd2022_TEST.cc

parametric_kmpw2010_TEST_SOURCES = parametric-kmpw2010_TEST.cc

pi_lcdas_TEST_SOURCES = pi-lcdas_TEST.cc

unitarity_bounds_TEST_SOURCES = unitarity-bounds_TEST.cc


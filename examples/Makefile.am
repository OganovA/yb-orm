
if NO_STD_STRING
TUTORIAL_DIR=
else
TUTORIAL_DIR=tutorial
endif

SUBDIRS=domain . $(TUTORIAL_DIR)
AUTOMAKE_OPTIONS = subdir-objects

AM_CXXFLAGS = \
	-I $(top_srcdir)/include/yb \
	$(XML_CPPFLAGS) \
	$(BOOST_CPPFLAGS) \
	$(SQLITE3_CFLAGS) \
	$(SOCI_CXXFLAGS) \
	$(WX_CFLAGS) \
	$(QT_CFLAGS)

noinst_PROGRAMS=example1 example2

example1_SOURCES=example1.cpp domain/Client.cpp domain/Order.cpp \
	domain/Product.cpp domain/ProductGroup.cpp domain/Contract.cpp \
	domain/OrderItem.cpp

example1_LDFLAGS = \
	$(top_builddir)/src/orm/libyborm.la \
	$(top_builddir)/src/util/libybutil.la \
	$(XML_LIBS) \
	$(BOOST_THREAD_LDFLAGS) \
	$(BOOST_THREAD_LIBS) $(BOOST_DATE_TIME_LIBS) \
	$(ODBC_LIBS) \
	$(SQLITE3_LIBS) \
	$(SOCI_LIBS) \
	$(WX_LIBS) \
	$(QT_LDFLAGS) \
	$(QT_LIBS) \
	$(EXECINFO_LIBS)

example2_SOURCES=example2.cpp domain/Client.cpp domain/Order.cpp \
	domain/Product.cpp domain/ProductGroup.cpp domain/Contract.cpp \
	domain/OrderItem.cpp domain/Payment.cpp domain/CCardPayment.cpp

example2_LDFLAGS = \
	$(top_builddir)/src/orm/libyborm.la \
	$(top_builddir)/src/util/libybutil.la \
	$(XML_LIBS) \
	$(BOOST_THREAD_LDFLAGS) \
	$(BOOST_THREAD_LIBS) $(BOOST_DATE_TIME_LIBS) \
	$(ODBC_LIBS) \
	$(SQLITE3_LIBS) \
	$(SOCI_LIBS) \
	$(WX_LIBS) \
	$(QT_LDFLAGS) \
	$(QT_LIBS) \
	$(EXECINFO_LIBS)


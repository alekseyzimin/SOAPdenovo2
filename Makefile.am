ACLOCAL_AMFLAGS = -I m4
noinst_LIBRARIES = libstandard63.a libsparse63.a libstandard127.a libsparse127.a
bin_PROGRAMS = SOAPdenovo-63mer SOAPdenovo-127mer
AM_LDFLAGS = -lbam -lrt -lz -pthread -lm -Wl,--hash-style=both
AM_CPPFLAGS =
AM_CFLAGS = -O3
AM_CXXFLAGS = -O3

CPPFLAGS_63 = -D_63MER_ $(AM_CPPFLAGS)
CPPFLAGS_127 = -D_127MER_ $(AM_CPPFLAGS)

noinst_HEADERS = $(srcdir)/standardPregraph/inc/* $(srcdir)/sparsePregraph/inc/*

standard_SRCS = standardPregraph/arc.c					\
                standardPregraph/attachPEinfo.c				\
                standardPregraph/bubble.c standardPregraph/check.c	\
                standardPregraph/compactEdge.c				\
                standardPregraph/concatenateEdge.c			\
                standardPregraph/connect.c standardPregraph/contig.c	\
                standardPregraph/cutTipPreGraph.c			\
                standardPregraph/cutTip_graph.c				\
                standardPregraph/darray.c standardPregraph/dfib.c	\
                standardPregraph/dfibHeap.c standardPregraph/fib.c	\
                standardPregraph/fibHeap.c				\
                standardPregraph/hashFunction.c				\
                standardPregraph/kmer.c standardPregraph/lib.c		\
                standardPregraph/loadGraph.c				\
                standardPregraph/loadPath.c				\
                standardPregraph/loadPreGraph.c				\
                standardPregraph/localAsm.c standardPregraph/map.c	\
                standardPregraph/mem_manager.c				\
                standardPregraph/newhash.c				\
                standardPregraph/node2edge.c				\
                standardPregraph/orderContig.c				\
                standardPregraph/output_contig.c			\
                standardPregraph/output_pregraph.c			\
                standardPregraph/output_scaffold.c			\
                standardPregraph/pregraph.c				\
                standardPregraph/prlHashCtg.c				\
                standardPregraph/prlHashReads.c				\
                standardPregraph/prlRead2Ctg.c				\
                standardPregraph/prlRead2path.c				\
                standardPregraph/prlReadFillGap.c			\
                standardPregraph/read2scaf.c				\
                standardPregraph/readInterval.c				\
                standardPregraph/stack.c				\
                standardPregraph/readseq1by1.c				\
                standardPregraph/scaffold.c				\
                standardPregraph/searchPath.c standardPregraph/seq.c	\
                standardPregraph/splitReps.c				\
                standardPregraph/cutTip_graph2.c			\
                standardPregraph/linearEdge.c				\
                standardPregraph/kmerhash.c				\
                standardPregraph/read2edge.c				\
                standardPregraph/iterate.c

sparse_SRCS = sparsePregraph/build_graph.cpp				\
              sparsePregraph/build_edge.cpp				\
              sparsePregraph/multi_threads.cpp				\
              sparsePregraph/build_preArc.cpp				\
              sparsePregraph/pregraph_sparse.cpp			\
              sparsePregraph/io_func.cpp sparsePregraph/global.cpp	\
              sparsePregraph/convert_soapdenovo.cpp

# 63 mer
libstandard63_a_SOURCES = $(standard_SRCS)
libstandard63_a_CPPFLAGS = $(CPPFLAGS_63) -I$(srcdir)/standardPregraph/inc

libsparse63_a_SOURCES = $(sparse_SRCS)
libsparse63_a_CPPFLAGS = $(CPPFLAGS_63) -I$(srcdir)/sparsePregraph/inc

SOAPdenovo_63mer_SOURCES = standardPregraph/main.c
SOAPdenovo_63mer_CPPFLAGS = $(CPPFLAGS_63) -I$(srcdir)/standardPregraph/inc
SOAPdenovo_63mer_LDADD = libstandard63.a libsparse63.a
SOAPdenovo_63mer_LINK = $(CXXLINK)

# 127 mer
libstandard127_a_SOURCES = $(standard_SRCS)
libstandard127_a_CPPFLAGS = $(CPPFLAGS_127) -I$(srcdir)/standardPregraph/inc

libsparse127_a_SOURCES = $(sparse_SRCS)
libsparse127_a_CPPFLAGS = $(CPPFLAGS_127) -I$(srcdir)/sparsePregraph/inc

SOAPdenovo_127mer_SOURCES = standardPregraph/main.c
SOAPdenovo_127mer_CPPFLAGS = $(CPPFLAGS_127) -I$(srcdir)/standardPregraph/inc
SOAPdenovo_127mer_LDADD = libstandard127.a libsparse127.a
SOAPdenovo_127mer_LINK = $(CXXLINK)


all:
EXTRA_CXXFLAGS = -Wno-sign-compare
include ../kaldi.mk

LDFLAGS += $(CUDA_LDFLAGS)
LDLIBS += $(CUDA_LDLIBS)

BINFILES = chain-est-phone-lm chain-get-supervision chain-make-den-fst \
        nnet3-chain-get-egs nnet3-chain-copy-egs nnet3-chain-merge-egs \
        nnet3-chain-shuffle-egs nnet3-chain-subset-egs \
        nnet3-chain-acc-lda-stats nnet3-chain-train nnet3-chain-compute-prob \
        nnet3-chain-combine nnet3-chain-normalize-egs


OBJFILES =

# Add this dependency to force cuda-compiled.o to be rebuilt when we reconfigure.
cuda-compiled.o: ../kaldi.mk

TESTFILES =

ADDLIBS = ../nnet3/kaldi-nnet3.a ../chain/kaldi-chain.a ../gmm/kaldi-gmm.a \
         ../decoder/kaldi-decoder.a ../lat/kaldi-lat.a ../hmm/kaldi-hmm.a  \
         ../transform/kaldi-transform.a ../tree/kaldi-tree.a \
         ../thread/kaldi-thread.a ../cudamatrix/kaldi-cudamatrix.a \
         ../matrix/kaldi-matrix.a ../fstext/kaldi-fstext.a \
         ../util/kaldi-util.a ../base/kaldi-base.a

include ../makefiles/default_rules.mk
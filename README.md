This is a collection of programs and modules, written in C, that
support research and education concerning Low Density Parity Check
(LDPC) codes.

See index.html in this directory for an index to the documentation.
Copyright information can be found there, and in the file COPYRIGHT.

Website with documentation: https://shubhamchandak94.github.io/LDPC-codes/

----

This is a fork of https://github.com/radfordneal/LDPC-codes with two major additions:
1. Miscellaneous channel - the original repository provided a few channels for decoding,
 such as binary symmetric channel (BSC) and the additive white Gaussian noise (AWGN) channel.
 However in many applications other channels are required. In general, the LDPC
 decoding requires the channel only to compute the log-likelihood ratio (LLR). Thus,
 we introduce a misc channel where the input to the LDPC decoder are the LLRs.
 For any given channel, the LLRs can be computed from the received message and then the decoding can be
 run with the misc channel. More details are provided [here](https://shubhamchandak94.github.io/LDPC-codes/channel.html) and [here](http://shubhamchandak94.github.io/LDPC-codes/decoding.html#decode).
 This channel was utilized in https://github.com/shubhamchandak94/LDPC_DNA_storage for applying
 LDPC codes for DNA storage, and was also used to enable puncturing in an extension of this library to
 handle protograph LDPC codes (https://shubhamchandak94.github.io/ProtographLDPC/).

 2. Extracting systematic bits position - The original library provides an extract functionality to obtain the
 message bits from the codeword. We provide an additional method to extract the positions of these bits in the codeword. This
 can be useful for certain applications where we need to know where where the message bits reside within the codeword.
 The documentation is available [here](https://shubhamchandak94.github.io/LDPC-codes/support.html#extract_systematic).

 Also see https://github.com/shubhamchandak94/ProtographLDPC/ which
 extends this library to construct protograph LDPC codes which can provide
 both near-optimal asymptotic performance and excellent finite-block performance.

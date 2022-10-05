cmake_minimum_required (VERSION 3.21)
project (SimpleFasta)
enable_testing()

add_executable(fasta-recs src/fasta-recs.c src/fasta.c)
add_executable(get-subseqs src/get-subseqs.c src/fasta.c)

add_test(fasta-recs .test/test-fasta-recs.sh)
add_test(get-subseqs .test/test-get-subseqs.sh)

CC=g++ -std=c++0x

#use path according to boost installation directory in user machine
export LD_LIBRARY_PATH=../boost_1_78_0/lib:$LD_LIBRARY_PATH 

#use paths according to boost installation directory in user machine
CFLAGS= -I../boost_1_78_0/include -L../boost_1_78_0/lib -O2 -ggdb -lboost_thread -lpthread -lboost_system

##### source files #####
# preprocessing
PREP=preproc/preproc.cpp preproc/preproc_new.cpp preproc/run_pre.cpp
# edge computation
COMPUTATION=edgecomp/engine.cpp edgecomp/compute.cpp edgecomp/edgemerger.cpp edgecomp/repart.cpp
LOADER=datastructures/loader.cpp edgecomp/grammar.cpp
# computation sets included through header files
DATASTRUCTS=datastructures/vertex.cpp datastructures/loadedvertexinterval.cpp datastructures/minset.cpp datastructures/partition.cpp datastructures/context.cpp datastructures/vit.cpp datastructures/DDM.cpp
UTIL=../test/timer.cpp Library/Logger.cpp

##### build rules #####
comp: dispatcher/graspan.cpp $(PREP) $(LOADER) $(COMPUTATION) $(DATASTRUCTS) $(UTIL)
	$(CC) dispatcher/graspan.cpp $(PREP) $(LOADER) $(COMPUTATION) $(DATASTRUCTS) $(UTIL) -o ../bin/comp -I../boost_1_78_0/include -L../boost_1_78_0/lib -O2 -ggdb -lboost_thread -lpthread -lboost_system


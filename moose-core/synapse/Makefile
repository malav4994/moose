#/**********************************************************************
#** This program is part of 'MOOSE', the
#** Messaging Object Oriented Simulation Environment.
#**           copyright (C) 2007 Upinder S. Bhalla. and NCBS
#** It is made available under the terms of the
#** GNU Lesser General Public License version 2.1
#** See the file COPYING.LIB for the full notice.
#**********************************************************************/

TARGET = _synapse.o

OBJ = \
	SynHandlerBase.o	\
	SimpleSynHandler.o	\
	STDPSynHandler.o	\
	GraupnerBrunel2012CaPlasticitySynHandler.o	\
	Synapse.o	\
	STDPSynapse.o	\
	RollingMatrix.o	\
	SeqSynHandler.o \
	testSynapse.o	\

# GSL_LIBS = -L/usr/lib -lgsl

HEADERS = \
	../basecode/header.h \
	../utility/numutil.h \


default: $(TARGET)

$(OBJ)	: $(HEADERS)
SynHandlerBase.o:	SynHandlerBase.h Synapse.h 
SimpleSynHandler.o:	SynHandlerBase.h Synapse.h SimpleSynHandler.h SynEvent.h
STDPSynHandler.o:	SynHandlerBase.h STDPSynapse.h STDPSynHandler.h SynEvent.h
GraupnerBrunel2012CaPlasticitySynHandler.o:	SynHandlerBase.h Synapse.h GraupnerBrunel2012CaPlasticitySynHandler.h SynEvent.h
Synapse.o:	Synapse.h SynHandlerBase.h
STDPSynapse.o:	STDPSynapse.h SynHandlerBase.h
RollingMatrix.o:	RollingMatrix.h
SeqSynHandler.o:	SynHandlerBase.h Synapse.h SimpleSynHandler.h SeqSynHandler.h RollingMatrix.h SynEvent.h
testSynapse.o: SynHandlerBase.h Synapse.h SimpleSynHandler.h SeqSynHandler.h RollingMatrix.h SynEvent.h

.cpp.o:
	$(CXX) $(CXXFLAGS) $(SMOLDYN_FLAGS) -I. -I../basecode -I../msg -I .. -I../external/muparser/include $< -c

$(TARGET): $(OBJ) $(SMOLDYN_OBJ) $(HEADERS)
	$(LD) -r -o $(TARGET) $(OBJ) $(SMOLDYN_OBJ) $(SMOLDYN_LIB_PATH) $(SMOLDYN_LIBS) $(GSL_LIBS)

clean:
	rm -f *.o $(TARGET) core core.*

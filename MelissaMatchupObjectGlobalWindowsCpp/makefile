# Melissa MatchUp Object Windows C++

CXX=cl
CXXFLAGS=-Zi -EHsc /std:c++17
LDLIBS=mdMatchUp.lib
RM=del /q /f

all: MelissaMatchupObjectGlobalWindowsCpp.exe clean

MelissaMatchupObjectGlobalWindowsCpp.exe: Main.cpp mdMatchup.h mdMatchUpEnums.h
    $(CXX) $(CXXFLAGS) Main.cpp MatchupObjectGlobal.cpp $(LDLIBS) /Fe:.\Build\MelissaMatchupObjectGlobalWindowsCpp.exe

clean:
    $(RM) *.obj *.ilk *.pdb *.h.hash *.lib.hash 



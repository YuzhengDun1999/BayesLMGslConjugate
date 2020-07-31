JAVA_HOME = ..
SRC = $(JAVA_HOME)/src

# For package BayesLMCConjugate
JC = javac
JFLAGS = -d
JAVA_SRC = $(SRC)/BayesLMC.java $(SRC)/fileinput.java
PACKAGE = $(JAVA_HOME)/class/BayesLMCConjugate
SUBPACKAGES_CLASS_PATH = $(JAVA_HOME)/class

all: subpackage $(PACKAGE)

.PHONY: subpackage

subpackage:
	@mkdir -p $(@D)
	$(MAKE) -C ../JAMAJniGsl/src

$(PACKAGE): $(JAVA_SRC)
	@mkdir -p $(@D)
	$(JC) $(JFLAGS) $(JAVA_HOME)/class -classpath $(SUBPACKAGES_CLASS_PATH):. $(JAVA_SRC)

clean: 
	rm -fr $(JAVA_HOME)/class
	rm -fr $(JAVA_HOME)/lib

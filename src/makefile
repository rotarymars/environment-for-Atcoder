BIN = ./a.exe
DEBUG_BIN = ./debug.exe
SOURCE_FILE = ./main.cpp
SAMPLE_PATH = ./test
all: $(BIN) $(SAMPLE_PATH)
	python ../oj_helper.py ts $(SOURCE_FILE)
$(DEBUG_BIN): $(SOURCE_FILE)
	g++ -std=gnu++23 -o "debug.exe" -D_DEBUG $(SOURCE_FILE)
$(BIN): $(SOURCE_FILE)
	g++ -std=gnu++23 -o "a.exe" $(SOURCE_FILE)
$(SAMPLE_PATH):
	python ../oj_helper.py d
submit: $(SOURCE_FILE)
	python ../oj_helper.py s $(SOURCE_FILE)
debugtest: $(DEBUG_BIN) $(SAMPLE_PATH)
	oj t -c $(DEBUG_BIN)

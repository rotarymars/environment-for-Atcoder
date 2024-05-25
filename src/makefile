BIN = ./a.exe
DEBUG_BIN = ./debug.exe
SOURCE_FILE = main.cpp
SAMPLE_PATH = ./test/sample-1.in
all: $(BIN) $(SAMPLE_PATH)
	python ../oj_helper.py ts $(SOURCE_FILE)
download: $(SAMPLE_PATH)
$(DEBUG_BIN): $(SOURCE_FILE)
	g++ -std=gnu++23 -o "debug.exe" -D_DEBUG $(SOURCE_FILE)
test: $(DEBUG_BIN) $(SAMPLE_PATH)
	oj t -c "./debug.exe"
$(BIN): $(SOURCE_FILE)
	g++ -std=gnu++23 -o "a.exe" $(SOURCE_FILE)
$(SAMPLE_PATH):
	python ../oj_helper.py d

# Remember to add the -DBIG_TARGET option to the CFLAGS in case we are compiling for a big endian system

TARGETS = deepCalls testAdd1 testChar1 testConv1 testConv2 testDiv1 testDiv2 testDiv3  testDiv4 testDiv5  testDouble  testDouble2 testDouble3  testLoadByte1 testLoadByte2 testLoadByte3 testLoadDouble testLoadHalf testLogic1 testLogic2 testLoop1 testLoop10 testLoop2 testLoop3 testLoop4 testLoop5 testLoop6 testLoop7 testLoop8 testLoop9 testMul1 testShift1 testShift2 testShift3 testStoreByte1 testStoreByte2 testStoreDouble testStoreHalf testStoreDouble2

all: $(TARGETS)

$(TARGETS): $(addsuffix .c, $@)
	$(CC) -o $@ -g3 $(CFLAGS) $(addsuffix .c, $@)

clean:
	rm $(TARGETS) $(addsuffix .trace, $(TARGETS)) $(addsuffix .dmp, $(TARGETS)) *~ -rf

test: $(TARGETS)
	python executeTests.py $(SIMULATOR) $(TARGETS)
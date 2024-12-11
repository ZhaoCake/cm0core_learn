TOPNAME = CM0_SoC

V_SRC := $(shell find ../rtl -name "*.v" -o -name "*.sv")
C_SRC := $(shell find ./csrc -name "*.cpp" -o -name "*.c")
INCLUDE := -I ./csrc/include

vela:
	verilator --top-module $(TOPNAME) --trace --exe --cc -j 0 \
		--build $(C_SRC) $(V_SRC) --CFLAGS "-g $(INCLUDE) $(LLVM_CXXFLAGS) -mcmodel=large -O2"   

clean:
	rm -rf obj_dir
	@# 如果有vcd文件，也要删除
	if [ -f $(TOPNAME).vcd ]; then rm $(TOPNAME).vcd; fi

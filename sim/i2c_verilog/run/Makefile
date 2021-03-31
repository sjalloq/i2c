I2C=../../../
BENCH=$(I2C)/bench


work:
	vlib work

compile:
	vlog +libext+.v \
	+define+WAVES \
	+incdir+$(BENCH)/verilog \
	+incdir+$(I2C)/rtl/verilog \
	$(I2C)/rtl/verilog/i2c_master_bit_ctrl.v \
	$(I2C)/rtl/verilog/i2c_master_byte_ctrl.v \
	$(I2C)/rtl/verilog/i2c_master_top.v \
	$(BENCH)/verilog/i2c_slave_model.v \
	$(BENCH)/verilog/wb_master_model.v \
	$(BENCH)/verilog/modelsim_tb_top.v

sim:
	vsim -voptargs="+acc=rnp" tst_bench_top

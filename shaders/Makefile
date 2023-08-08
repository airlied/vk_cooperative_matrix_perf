# Copyright 2023 Intel Corporation
# SPDX-License-Identifier: MIT

all: tiledfp16.spv tiledfp32.spv tileds8.spv tiledu8.spv \
	shmemfp16.spv shmemfp32.spv shmems8.spv shmemu8.spv

tiledfp16.spv: tiled.comp
	glslang -DA_BITS=16 -DA_TYPE=float16_t -DC_TYPE=float16_t -V $< -o $@

tiledfp32.spv: tiled.comp
	glslang -DA_BITS=16 -DA_TYPE=float16_t -DC_TYPE=float     -V $< -o $@

tileds8.spv: tiled.comp
	glslang -DA_BITS=8 -DA_TYPE=int8_t -DC_TYPE=int32_t -V $< -o $@

tiledu8.spv: tiled.comp
	glslang -DA_BITS=8 -DA_TYPE=uint8_t -DC_TYPE=uint32_t -V $< -o $@

shmemfp16.spv: shmem.comp
	glslang -DA_BITS=16 -DA_TYPE=float16_t -DC_TYPE=float16_t -V $< -o $@

shmemfp32.spv: shmem.comp
	glslang -DA_BITS=16 -DA_TYPE=float16_t -DC_TYPE=float     -V $< -o $@

shmems8.spv: shmem.comp
	glslang -DA_BITS=8 -DA_TYPE=int8_t -DC_TYPE=int32_t -V $< -o $@

shmemu8.spv: shmem.comp
	glslang -DA_BITS=8 -DA_TYPE=uint8_t -DC_TYPE=uint32_t -V $< -o $@

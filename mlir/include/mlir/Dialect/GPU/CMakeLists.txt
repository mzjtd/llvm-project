add_mlir_dialect(GPUOps gpu)
add_mlir_doc(GPUOps -gen-op-doc GPUOps Dialects/)

set(LLVM_TARGET_DEFINITIONS ParallelLoopMapperAttr.td)
mlir_tablegen(ParallelLoopMapperAttr.h.inc -gen-struct-attr-decls)
mlir_tablegen(ParallelLoopMapperAttr.cpp.inc -gen-struct-attr-defs)
add_public_tablegen_target(MLIRParallelLoopMapperAttrGen)

set(LLVM_TARGET_DEFINITIONS ParallelLoopMapperAttr.td)
mlir_tablegen(ParallelLoopMapperEnums.h.inc -gen-enum-decls)
mlir_tablegen(ParallelLoopMapperEnums.cpp.inc -gen-enum-defs)
add_public_tablegen_target(MLIRParallelLoopMapperEnumsGen)

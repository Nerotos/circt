set(LLVM_LINK_COMPONENTS
  Support
)

add_circt_tool(om-linker
  om-linker.cpp
)
llvm_update_compile_flags(om-linker)
target_link_libraries(om-linker PRIVATE
  CIRCTComb
  CIRCTEmit
  CIRCTHW
  CIRCTOM
  CIRCTOMTransforms
  CIRCTSV
  CIRCTSupport
  CIRCTVerif

  MLIRBytecodeReader
  MLIRBytecodeWriter
  MLIRParser
  MLIRSupport
  MLIRIR
  MLIROptLib
)

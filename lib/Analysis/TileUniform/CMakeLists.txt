if(WIN32 OR CYGWIN)
  set(LLVM_LINK_COMPONENTS Core Support Analysis)
endif()

add_llvm_loadable_module( LLVMTileUniform
  TileUniform.cpp
  )

add_dependencies(LLVMTileUniform intrinsics_gen)

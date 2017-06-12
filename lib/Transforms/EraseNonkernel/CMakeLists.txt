if(WIN32 OR CYGWIN)
  set(LLVM_LINK_COMPONENTS Core Support Analysis)
endif()


add_llvm_loadable_module( LLVMEraseNonkernel
  EraseNonkernel.cpp
  )

add_dependencies(LLVMEraseNonkernel intrinsics_gen)

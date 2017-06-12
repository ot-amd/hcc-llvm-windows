if(WIN32 OR CYGWIN)
  set(LLVM_LINK_COMPONENTS Core Support)
endif()


add_llvm_loadable_module( LLVMCpuRename
    CpuRename.cpp
  )

add_dependencies(LLVMCpuRename intrinsics_gen)

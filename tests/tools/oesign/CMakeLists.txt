# Copyright (c) Open Enclave SDK contributors.
# Licensed under the MIT License.

add_subdirectory(test-enclave)
add_subdirectory(test-inputs)

if (NOT WIN32)
  # Windows version of oesign does not use openssl, therefore there is no openssl engine support and
  # not much sense in trying to test it.
  add_subdirectory(test-engine)
endif ()

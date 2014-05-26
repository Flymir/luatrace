# Copyright (C) 2014 Tai Chi Minh Ralph Eastwood.
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with Flymir LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luatrace C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module ( c_hook c/c_hook.c )
install_lua_module ( luatrace lua/luatrace.lua )
install_lua_module ( luatrace.profile lua/luatrace/profile.lua )
install_lua_module ( luatrace.trace_file lua/luatrace/trace_file.lua )
install_lua_module ( uatrace lua/uatrace.lua )
install_lua_module ( uatrace.profile lua/uatrace/profile.lua )
install_lua_module ( jit.annotate lua/jit/annotate.lua )
install_data ( README.md LICENSE AUTHORS )
install ( PROGRAMS ${CMAKE_SOURCE_DIR}/sh/luatrace.profile DESTINATION bin )

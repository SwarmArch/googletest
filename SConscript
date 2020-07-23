from __future__ import (absolute_import, division, print_function)

Import('env')

localenv = env.Clone()

gtest_include_path = Dir('.').srcnode().abspath + '/googletest/include'

localenv.Append(CPPPATH = [gtest_include_path, 'googletest'])

libgtest = localenv.StaticLibrary(
        target = 'gtest',
        source = ['googletest/src/gtest-all.cc'])
libgtest_main = localenv.StaticLibrary(
        target = 'gtest_main',
        source = ['googletest/src/gtest-all.cc', 'googletest/src/gtest_main.cc'])

Return('gtest_include_path', 'libgtest', 'libgtest_main')

project('SynthLauncher', 'cpp', license: 'aGPL-3.0', version: '1.0.0', license_files: 'LICENSE', default_options: ['cpp_std=c++17', 'warning_level=3'])

src = [
  'src/http/builder.cc',
  'src/http/parser.cc'
]

test_src = [
  'test/test.cc',
  'test/http.cc'
]

# Build dependency
simdjson = dependency('simdjson', required: true)

# Test dependency
gtest = dependency('gtest', required: false)

executable('SynthLauncher', [src, 'src/main.cc'], include_directories: 'include', dependencies: [simdjson])

test_exe = executable('SynthLauncherTest', [src, test_src], dependencies: [gtest, simdjson])

test('SynthLauncherTest', test_exe)

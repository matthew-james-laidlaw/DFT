include(GoogleTest)

add_executable(
    TestDFT
        TestFFT.cpp
        TestNaiveDFT.cpp
        Utils.cpp
)

target_link_libraries(
    TestDFT
        dft
        GTest::gtest_main
)

gtest_discover_tests(TestDFT)

add_executable(
    BenchmarkDFT
        BenchmarkFFT.cpp
        BenchmarkNaiveDFT.cpp
        Utils.cpp
)

target_link_libraries(
    BenchmarkDFT
        dft
        benchmark::benchmark_main
)

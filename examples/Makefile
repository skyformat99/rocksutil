include ../make_config.mk
	
.PHONY: clean librocksutil

all: log_example mutexlock_example thread_local_example thread_pool_example

log_example: librocksutil log_example.cc
	$(CXX) $(CXXFLAGS) $@.cc -o$@ ../librocksutil.a -I../ -I../include -O2 -std=c++11 $(PLATFORM_LDFLAGS) $(PLATFORM_CXXFLAGS)

mutexlock_example: librocksutil mutexlock_example.cc
	$(CXX) $(CXXFLAGS) $@.cc -o$@ ../librocksutil.a -I../ -I../include -O2 -std=c++11 $(PLATFORM_LDFLAGS) $(PLATFORM_CXXFLAGS)

thread_local_example: librocksutil thread_local_example.cc
	$(CXX) $(CXXFLAGS) $@.cc -o$@ ../librocksutil.a -I../ -I../include -O2 -std=c++11 $(PLATFORM_LDFLAGS) $(PLATFORM_CXXFLAGS)

thread_pool_example: librocksutil thread_pool_example.cc
	$(CXX) $(CXXFLAGS) $@.cc -o$@ ../librocksutil.a -I../ -I../include -O2 -std=c++11 $(PLATFORM_LDFLAGS) $(PLATFORM_CXXFLAGS)

clean:
	find . -name "*.[oda]" -exec rm -f {} \;
	rm -rf ./log_example ./mutexlock_example ./thread_local_example ./thread_pool_example

librocksutil:
	cd .. && $(MAKE) static_lib

FROM enumack/buildcontainers:clang-4.0

RUN apt-get update && apt-get install git -y && apt-get upgrade -y

RUN git clone -q https://github.com/google/googletest.git /googletest \
  && mkdir -p /googletest/build \
  && cd /googletest/build \
  && cmake .. && make && make install \
  && cd / && rm -rf /googletest

RUN apt-get --purge remove git -y && apt-get update && apt-get upgrade -y

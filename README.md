cl_examples
===========

Extracted from:

https://github.com/tonyrog/cl/tree/master/examples


##How to run

Clone, get CL OpenCL Erlang library and compile:

```bash
rebar clone 
cd cl_examples
rebar get-deps
rebar compile
```

Run from Erlang shell:

```erlang
ERL_LIBS=deps/:.
[cl_examples (master)]$ erl
Erlang R15B03 (erts-5.9.3.1) [source] [smp:2:2] [async-threads:0] [hipe] [kernel-poll:false]

Eshell V5.9.3.1  (abort with ^G)
1> application:start(cl).
ok
2> cl_bandwidth:test().
platform created
Testing with byte size: 4194304 
input memory created
queue created
Bandwidth tested with write size: 4194304 bytes

Write total milliseconds: 0.091
Bandwidth rate: 45010989 KB per second

Queue total milliseconds: 0.036
Bandwidth rate: 113777777 KB per second

ok
3> 
```

or (not tested - since I have no OpenGL):


``` erlang
[cl_examples (master)]$ ERL_LIBS=deps/:.
[cl_examples (master)]$ erl
Erlang R15B03 (erts-5.9.3.1) [source] [smp:2:2] [async-threads:0] [hipe] [kernel-poll:false]

Eshell V5.9.3.1  (abort with ^G)
1> application:start(cl).
ok
2> cc_subdiv:start().
...
```




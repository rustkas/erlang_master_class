# Erlang master class additional material

Lifehacks of practical usage source code examples.

## Master class 2

`demo2.erl`
```
% testing source code by any input (without hanging)
% pay attention to usage of function f(). It remove variable `Replay` from process memory

Pid1 = spawn(demo2, area, []).
Pid1 !{self(), {square, 20}}, f(Reply), receive Reply -> Reply end.
Pid1 !{self(), {square, 30}}, f(Reply), receive Reply -> Reply end.
Pid1 !{self(), {square, 40}}, f(Reply), receive Reply -> Reply end.
Pid1 !{self(), {square, 50}}, f(Reply), receive Reply -> Reply end.
```

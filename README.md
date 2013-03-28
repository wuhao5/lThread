lThread
=======

A combined and simplified version of lualanes and luaproc

## Feature (or not)
* Creation of a thread is intended to be separate in order to avoid the literal scope (either created from a file or a string)
* Only messaging is supported to reduce the complexity of locks, race conditions
* Linda from lualanes as messaging pipes while the data type is limited to keep simplicity (only primitive types: number,
string, boolean, table (no metatable), function (closures of primitive types) )
* threads might be pooled

## Lua
### thread.create(source, parameters)
### lyield.yield(thread) (see lyield)
### thread:join

the calling thread will be suspended

### thread:done
### thread:returns

if nothing is returned, it could be either that thread is not finished, or thread returns nothing. so check thread:done first

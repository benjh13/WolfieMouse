# Coding conventions
## Tabs and spaces
**There is no tabs, tabs should be equivalent to *two spaces***. There is a auto formatter in Atollic TrueSTUDIO. We can easily use it to fit our format.
## Naming convention
The basic naming convention is inspired by [FreeRTOS' coding convention](http://www.freertos.org/FreeRTOS-Coding-Standard-and-Style-Guide.html).

We use  mixed C and C++, however, each one has different naming conventions.

### file name
* In C. the all name is in lower case with an underscore to separate between words

ex.) `uart.h` `motor_driver.h`.

* In C++. The first letter of each words are in upper case, without underscore.

ex.) `UART.h` `MotorDriver.h`


### variable name
* Variables of type `uint32_t` are prefixed `uw`, where the `u` denotes `unsigned` and the `w` denotes `word`.

* Variables of type `uint16_t` are prefixed `uh`, where the `u` denotes `unsigned` and the `h` denotes `half word`.

* Variables of type `uint8_t` are prefixed `uc`, where the `u` denotes `unsigned` and the `c` denotes `char`.
* Variables of `signed` types are prefixed `s` instead of `u` for `unsigned` variables

* Enumerated variables are prefixed `e`

* Variables of non stdint types are prefixed `x`. Examples include `BaseType_t` and `TickType_t`, which are portable layer defined typedefs for the natural or most efficient type for the architecture and the type used to hold the RTOS tick count respectively.

* Unsigned variables of non stdint types have an additional prefix u. For example variables of type `UBaseType_t` (unsigned BaseType_t) are prefixed `ux`.

* Variables of type size_t are also prefixed `x`.

* Pointers have an additional prefixed p, for example a pointer to a `uint16_t` will have prefix `puh`. 
* Arrays and multi-dimentional arrays also have dimentional number of addtional p. For example, `uint32_t ppuwMatrix[][]`.

### function name
* File `scope` static (private) functions are prefixed with `prv`.

* Functions are prefixed with their return type, as per the convention defined for variables, with the addition of the prefix `v` for `void`.

* Function names of C start with the name of the file in which they are defined. For example `vTaskDelete` is defined in `tasks.c`, and has a `void` return type.
* Function or method names of C++ doesn't start with the name of the file, since namespace do that job. For example `Task::vDelete` is defined in `Tasks.cpp`, and has a `void` return type. 
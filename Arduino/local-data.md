# Local Data

For many Arduino boards small amounts of data can be saved locally using the EEPROM package.

EEPROM should not be used in the following cases:

1. You have a large amount of variables (EEPROM's storage is very limited).
2. Variables change often (Each addresses hardware will become degraded and unreliable after about 100,000 writes).

## Saving Variables

When saving you must specify:

1. The address to save the value at
2. The value to save

``` C++
#include <EEPROM.h>

int save_address = 1
int value = 2

EEPROM.write(save_address, value);
```

## Reading Variables

When reading variables you simple provide the address where the variable is stored.

``` C++
int read_address = 1;

int value = EEPROM.read(read_address);
```

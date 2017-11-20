Sample data
```shell
*
# .....
xyz
abc
#EOD
*
# .....
opq
rst
#EOD
*
```
The code below split the sample data into two splited files by string #EOD as well as removing lines start with * or #
```shell
DATA_DIR=/tmp
FILE_NAME=source
awk 'BEGIN {i=1} /#EOD/{++i;next}/^[^#*]/{print > FILE_NAME"."i".dat"}' FILE_NAME=${FILE_NAME} ${DATA_DIR}/${FILE_NAME}
```
here is two output files
```shell
source.1.dat
xyz
abc
```
```shell
source.2.dat
opq
rst
```

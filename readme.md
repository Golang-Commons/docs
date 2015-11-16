#Golang-Commons

Golang Commons comes from small golang projects.

##List

[arrayOperations](https://github.com/adam-hanna/arrayOperations)
[file](https://github.com/toolkits/file)


##Docs

###array

*arrayCommons* series are based on [arrayOperations](https://github.com/adam-hanna/arrayOperations).

usage:`import "github.com/Golang-Commons/arrayCommons"`

####Intersect

`IntersectString(args...[]string) []string`

Find the intersection of two arrays.

```
a1 := ["1" "2" "2" "4" "6"]
a2 := ["2" "4" "5"]
arrayCommons.IntersectString(a1, a2)  >> ["2" "4"]
```

####Union

`UnionString(args...[]string) []string`

Find the union of two arrays.

```
a1 =: ["1" "2" "2" "4" "6"]
a2 := ["2" "4" "5"]
arrayCommons.UnionString(a1, a2) >> ["1" "2" "4" "5" "6"]
```

####Difference

`DifferenceString(args...[]string) []string`

Find the union of two arrays.

```
a1 := ["1" "2" "2" "4" "6"]
a2 := ["2" "4" "5"]
arrayCommons.DifferenceString(a1, a2) >> ["1" "5" "6"]
```

####Distinct

`DistinctString(args []string) []string`

Remove duplicate values from one arrayCommons.

```
a1 = ["1" "2" "2" "4" "6"];
arrayCommons.DistinctString(a1) >> ["1" "2" "4" "6"]
```

###file

*fileCommons* series are based on [file](https://github.com/toolkits/file).
usage:`import "github.com/Golang-Commons/fileCommons"`

####Read

```
fileCommons.ToString(filePath string) (string, error)
//read a file into a string
fileCommons.ToBytes(filePath string) ([]byte, error)
//read a file into a []byte
fileCommons.ToTrimString(filePath string) (string, error)
//read a file into a trimed string
fileCommons.ToUint64(filePath string) (uint64, error)
//read a file (which content is a number) to an uint64
fileCommons.ToInt64(filePath string) (int64, error)
//read a file (which content is a number) to an int64
```

####Write

```
fileCommons.WriteBytes(filePath string, b []byte) (int, error)
//write a []byte into a file
fileCommons.WriteString(filePath string, s string) (int, error)
//write a string into a file
```

###net

####Download


```
netCommons.Download(toFile string, url string) error
```


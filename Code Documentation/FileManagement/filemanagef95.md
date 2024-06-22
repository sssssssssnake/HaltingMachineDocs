

contains the #subroutine `readFile` and the logical #function `containsString`.

It also contains the private elements of 
  
```fortran
character(:), allocatable :: reusableFilePath
character(:), allocatable, dimension(:) :: mainFileContent
```

the readFile #subroutine has these paramaters:
```fortran
subroutine readFile(filePath, fileContents, endingLine)
	character(:), allocatable, intent(in) :: filePath
	character(:), allocatable, intent(out) :: fileContents(:)
	integer, intent(out) :: endingLine
```

And the containsString #function is as such

```fortran
logical function containsString(keyword, searchString) result(isInString)
	character(:), allocatable, intent(in) :: keyword
	character(:), allocatable, intent(in) :: searchString
```

There is also a private #subroutine that simply prints the status of a file given the iostat
```fortran
subroutine printFileStatus(status)
	integer, intent(in) :: status
```

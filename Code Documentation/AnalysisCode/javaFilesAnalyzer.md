
Contains public subroutines like the  `setMainFileContent`,  `findImportantJavaFiles` , `printMainFileContent` #subroutine 

Private variables:
```fortran
character(:), allocatable :: sourceDirectory
character(:), allocatable, dimension(:) :: javaImports
character(:), allocatable, dimension(:) :: javaPackages
character(:), dimension(:), allocatable :: mainFileContent
```

and contains the #type
```fortran
type :: JavaFile
	character(:), allocatable :: relativeFilePath
	character(:), allocatable :: className
	character(:), allocatable :: packageName
	character(:), allocatable, dimension(:) :: imports
end type JavaFile
```


The `setMainFileContent` #subroutine has these parameters

```fortran
subroutine setMainFileContent(fileContent)
	character(:), dimension(:), allocatable, intent(in) :: fileContent
```

The `findImportantJavaFiles` #subroutine  has these parameters

```fortran
subroutine findImportantJavaFiles(lastLine)
	integer, intent(in) :: lastLine
```

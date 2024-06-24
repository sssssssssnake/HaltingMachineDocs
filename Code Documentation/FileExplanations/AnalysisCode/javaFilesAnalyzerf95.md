
Contains public subroutines like the  `setMainFileContent`,  `findImportantJavaFiles` , `printMainFileContent` #subroutine. The analyzer also uses the JavaFile #type from [[javaAnalysisTypesf95]]

Private variables:
```fortran
character(:), allocatable :: sourceDirectory
character(:), allocatable, dimension(:) :: javaImports
character(:), allocatable, dimension(:) :: javaPackages

character(:), dimension(:), allocatable :: mainFileContent
type(JavaFile) :: mainFile
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

The setSourceDirectory #subroutine is used for setting the file path basically of the java file
```fortran
subroutine setSourceDirectory(directory)
	character(:), allocatable, intent(in) :: directory
```


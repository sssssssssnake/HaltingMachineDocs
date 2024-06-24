
Contains the #type `JavaFile` and `Import`

```fortran
type :: JavaFile
	character(:), allocatable :: relativeFilePath
	character(:), allocatable :: className
	character(:), allocatable :: packageName
	character(:), allocatable, dimension(:) :: imports
	type(Import), allocatable, dimension(:) :: importObjects
	
	contains
	procedure :: initializeJavaFile
	procedure :: printJavaFile
	procedure :: resolveImportsToPaths
end type JavaFile
```

```fortran
type :: Import
	character(:), allocatable :: originalImportText
	logical :: isStatic
	logical :: isWildcard
	character(:), allocatable :: importPath
	character(:), allocatable :: importName
end type Import
```

The #subroutine procedures for JavaFile are defined here:

```fortran
!> Is essentially a constructor for the JavaFile type
!! @param this The JavaFile object to be initialized you don't need to pass this in, it's done automatically by the compiler
!! @param relativeFilePath The relative file path of the Java file
!! @param className The name of the class in the Java
!! @param packageName The package name of the Java file
!! @param imports The imports of the Java file
subroutine initializeJavaFile(this, relativeFilePath, className, packageName, imports)
	class(JavaFile), intent(inout) :: this
	character(:), allocatable, intent(in) :: relativeFilePath
	character(:), allocatable, intent(in) :: className
	character(:), allocatable, intent(in) :: packageName
	character(:), allocatable, dimension(:), intent(in) :: imports
```

```fortran
subroutine printJavaFile(this)
	class(JavaFile), intent(in) :: this
```

```fortran
!> Converts the imports to paths and names
!! @param this The JavaFile object to be initialized you don't need to pass this in, it's done automatically by the compiler
subroutine resolveImportsToPaths(this)
	class(JavaFile), intent(inout) :: this
```

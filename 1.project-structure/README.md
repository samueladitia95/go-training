# 1. Project Structure

## Package

- Go project is organized into one or several packages.
- Each package must have a unique name.
- Each package must be in the same directory (_Even subdirectory not allowed_).
- Package `main` with function `main` needed as root.
- Same package can be at multiple files, as long as they are in the same directory (_Even subdirectory not allowed_)
- Internal variable or function that only used within the same package use camel case (_ex: camelCase_)
- If variable or function able to be exported outside package, use pascal case (_ex: PascalCase_)

## Module

- Multiple packages is called `Module`.
- Module is declare with `go.mod` files, with module name dan go version requirement.
- 1 package can be called by another package with `import` statement.

```go
import (
  "fmt"; // Base package
  "module_name/folder/package_name"; // Import another package from same module
  "github.com/routes_to_go_package"  // Import from remote repo
)
```

## How to Run

- `go run .` in module root directory

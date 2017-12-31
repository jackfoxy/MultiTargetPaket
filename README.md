# jftest

Muti-target dotnet restore problem with Paket

\<TargetFramework>net45\</TargetFramework>

\<TargetFramework>net47\</TargetFramework>

\<TargetFramework>netstandard2.0\</TargetFramework>

all build correctly,

but the multi-target builds

\<TargetFrameworks>net45;net47\</TargetFrameworks>

\<TargetFrameworks>net47;netstandard2.0\</TargetFrameworks>

fail to resolve the package reference Argu.

The multi-target builds have been verified to work when the project uses nuget package references instead of Paket.

See https://github.com/jackfoxy/MultiTargetNuget

## Reproduction steps

### every time the build targets change

- paket update -f 
- dotnet restore



Unithereum
==========

This UPM package enables Unity projects to interact with Ethereum-like
blockchain nodes.

Installation
------------

Open the Unity Package Manager and add a package from a git URL. The URL for
this package is:
`https://github.com/planetarium/Unithereum.git?path=/Unity/Assets/Plugins/Unithereum`.

Code Generation
---------------

This package contains a code generation script that creates C# classes that can
be used to interact with smart contracts from ABI and BIN (optional) artifacts
generated by [solc]. Code is generated whenever .abi and .bin files are added or
modified in the `Assets/` directory, or any subdirectory therein. To force
regeneration, you may reimport the desired files in the Unity Editor. Note that
code for preexisting .abi files will not be generated until they are reimported.

The generated code is placed in the `Assets/ContractServices/` directory, and
will be under the `{ProductName}.ContractServices` assembly. Please note that
the `ProductName` will be sanitized to qualify as a [C# identifier name].

[solc]: https://github.com/ethereum/solidity
[C# identifier name]: https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names

Building
--------

To build this project, you must have the Unity Editor 2021.3.19f installed.
Please make sure that Unity .meta files are generated before updating the
built package at `Assets/Plugins/Unithereum` (e.g. Open Unity project at
`Unity` with the Unity Editor and reimport new assets).
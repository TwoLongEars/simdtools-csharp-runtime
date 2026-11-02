# simdtools-csharp-runtime

The .NET 10 WebAssembly runtime, the Roslyn C# compiler and the .NET reference assemblies that SIMDTools' C# IDE downloads (on consent) to run C# in the browser. Each tag `vN` is one bundle, loaded through jsDelivr:

```
https://cdn.jsdelivr.net/gh/TwoLongEars/simdtools-csharp-runtime@vN/dist/
```

`dist/manifest.json` lists every file with its size and SHA-256; the IDE pins the SHA-256 of `manifest.json` itself, so a moved tag cannot swap the bundle.

The bundle is built from SIMDTools' `tools/csharp-runtime/` with `node scripts/build/build_csharp_runtime.mjs --version vN`. Never edit `dist/` by hand: publish a new tag instead.

## Licenses

The .NET runtime (`LICENSES/dotnet-runtime.txt`, third-party notices in `LICENSES/dotnet-runtime-third-party-notices.txt`), Roslyn (`LICENSES/roslyn.txt`) and Basic.Reference.Assemblies (`LICENSES/basic-reference-assemblies.txt`) are MIT licensed.

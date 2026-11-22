# Win32 metadata for language projections

`metadata/Microsoft.Direct3D.D3D12.winmd` describes the D3D12 APIs in this package's
headers for downstream language projections, such as CsWin32 for C# and windows-rs
for Rust. It preserves the `Windows.Win32.Graphics.Direct3D12` namespace.

## C# with CsWin32

Automatic discovery requires a `Microsoft.Windows.SDK.Win32Metadata` package
that supplies a separate D3D12 winmd, and a CsWin32 version that supports
cross-assembly COM types. Add both to your C# project along with this package.
The Agility metadata replaces the Windows SDK D3D12 baseline, so CsWin32 receives
only one D3D12 provider.

Native consumers do not acquire a dependency on either metadata package or CsWin32.

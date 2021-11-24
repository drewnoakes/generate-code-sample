# Generating code with MSBuild

This sample project shows how to generate code during a build, and have that generated code be included in that build.

The project is configured to work correctly with incremental build, for both builds inside VS and at the command line.

Generated code is emitted to the intermediate (i.e. `obj`) folder.

In this sample, the generated code includes a hash of the source file as a constant in C# code. The generation logic can be substituted for something else, depending upon your application.

The build customisation lives inside `Generator.props` and `Generator.targets`. It is likely that you would include these files inside a NuGet package. The consumer should not need to do anything special to their project other than reference that package and specify input items with the correct MSBuild item type.

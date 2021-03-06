GENERATED
---------

Is this source file generated as part of the build or CMake process.

Tells the internal CMake engine that a source file is generated by an outside
process such as another build step, or the execution of CMake itself. This
information is then used to exempt the file from any existence or validity
checks. Generated files are created by the execution of commands such as
:command:`add_custom_command` and :command:`file(GENERATE)`.

When a generated file created by an :command:`add_custom_command` command
is explicitly listed as a source file for any target in the same
directory scope (which usually means the same ``CMakeLists.txt`` file),
CMake will automatically create a dependency to make sure the file is
generated before building that target.

Generated sources may be hidden in some IDE tools, while in others they might
be shown. For the special case of sources generated by CMake's :prop_tgt:`AUTOMOC`
or :prop_tgt:`AUTORCC` functionality, the :prop_gbl:`AUTOGEN_SOURCE_GROUP`,
:prop_gbl:`AUTOMOC_SOURCE_GROUP` and :prop_gbl:`AUTORCC_SOURCE_GROUP` target
properties may influence where the generated sources are grouped in the project's
file lists.

# C/C++ for Visual Studio Code Change Log

## Version 0.26.1: October 28, 2019
### Bug Fixes
* Fix `launch.json` creation when using non-English display languages. [#4464](https://github.com/microsoft/vscode-cpptools/issues/4464)
* Fix CHS translation. [#4422](https://github.com/microsoft/vscode-cpptools/issues/4422)
* Fix debugging hang when Windows 10 Beta Unicode (UTF-8) support is enabled. [#1527](https://github.com/microsoft/vscode-cpptools/issues/1527)

## Version 0.26.0: October 15, 2019
### New Features
* Add localization support (translated text) via `Configure Display Language`. [#7](https://github.com/microsoft/vscode-cpptools/issues/7)
* Add `Rename Symbol` with a pending rename UI. [#296](https://github.com/microsoft/vscode-cpptools/issues/296),  [PR #4277](https://github.com/microsoft/vscode-cpptools/pull/4277)
* Add support for navigation breadcrumbs and nested symbols in the Outline view (and removed the Navigation status bar item). [#2230](https://github.com/microsoft/vscode-cpptools/issues/2230)
* Add support for C++/CX (`/ZW`, `/ZW:nostdlib`, `/FI`, `/FU`, and `/AI` compiler arguments). [#3039](https://github.com/microsoft/vscode-cpptools/issues/3039)
* Add a tree view UI for the other C++ references results. [#4079](https://github.com/microsoft/vscode-cpptools/issues/4079)

### Enhancements
* App support for .rsp files in `compile_commands.json`. [#1718](https://github.com/microsoft/vscode-cpptools/issues/1718)
* Add support for `SymbolLoadInfo` to `launch.json`. [#3324](https://github.com/microsoft/vscode-cpptools/issues/3324)
* Enable `${workspaceFolder}` in `compilerPath` and `compilerArgs`. [#3440](https://github.com/microsoft/vscode-cpptools/issues/3440)
* Add support for parsing more file types by default. [#3567](https://github.com/microsoft/vscode-cpptools/issues/3567)
* Move status icons to the left to minimize shifting and change the red flame to use the foreground color. [#4198](https://github.com/microsoft/vscode-cpptools/issues/4198)

### Bug Fixes
* Fix querying of non-ENU compilers. [#2874](https://github.com/microsoft/vscode-cpptools/issues/2874)
* Fix IntelliSense error with `constexpr const char* s[] = { "" }`. [#2939](https://github.com/microsoft/vscode-cpptools/issues/2939)
* Add support for C++20 designated initializers for cl and gcc. [#3491](https://github.com/Microsoft/vscode-cpptools/issues/3491)
* Fix `Find All References` not confirming references of method overrides in an inheritance hierarchy. [#4078](https://github.com/microsoft/vscode-cpptools/issues/4078)
* Fix missing references on the last line. [#4150](https://github.com/microsoft/vscode-cpptools/issues/4150)
* Fix `Go to Definition` on implicit default constructors. [#4162](https://github.com/microsoft/vscode-cpptools/issues/4162)
* Fix configuration prompts from appearing if a configuration provider is set. [#4168](https://github.com/microsoft/vscode-cpptools/issues/4168)
* Fix vcpkg code action for missing includes with more than one forward slash. [PR #4172](https://github.com/microsoft/vscode-cpptools/pull/4172)
* Fix parsing of `__has_include` (and other system macros) with gcc. [#4193](https://github.com/microsoft/vscode-cpptools/issues/4193)
* Fix tag parse database not getting updated after changes occur to unopened files in the workspace. [#4211](https://github.com/microsoft/vscode-cpptools/issues/4211)
* Fix `files.exclude` ending with `/` being treated like a per-file exclude (which aren't enabled by default). [#4262](https://github.com/microsoft/vscode-cpptools/issues/4262)
* Fix `Find All References` incorrect results for string and comment references. [#4279](https://github.com/microsoft/vscode-cpptools/issues/4279)
* Fix bug with forced includes in `compile_commands.json`. [#4293](https://github.com/microsoft/vscode-cpptools/issues/4293)
* Fix `Find All References` giving `Not a Reference` for constructors of templated classes. [#4345](https://github.com/microsoft/vscode-cpptools/issues/4345)
* Fix squiggles appearing after a multi-edit replace or rename. [#4351](https://github.com/microsoft/vscode-cpptools/issues/4351)
* Fix `gcc-x86` and `clang-x86` modes. [#4353](https://github.com/microsoft/vscode-cpptools/issues/4353)
* Fix crashes if the database can't be created. [#4359](https://github.com/microsoft/vscode-cpptools/issues/4359)
* Fix bugs with comment references. [#4371](https://github.com/microsoft/vscode-cpptools/issues/4371), [#4372](https://github.com/microsoft/vscode-cpptools/issues/4372)

## Version 0.25.1: August 28, 2019
### Bug Fixes
* Fix `Switch Header/Source` for `.H` and `.C` targets. [#3048](https://github.com/microsoft/vscode-cpptools/issues/3048)
* Fix `C_Cpp.updateChannel` not respecting `extensions.autoUpdate`. [#3632](https://github.com/microsoft/vscode-cpptools/issues/3632)
* Fix duplicate content appearing after formatting of a new file (2nd fix). [#4091](https://github.com/microsoft/vscode-cpptools/issues/4091)
* Fix links in `Log Diagnostics` output. [#4122](https://github.com/microsoft/vscode-cpptools/issues/4122)
* Fix `NullReferenceException` when debugging if `"description"` is missing. [#4125](https://github.com/microsoft/vscode-cpptools/issues/4125)
* Fix `files.exclude` processing when using `\\`. [#4127](https://github.com/microsoft/vscode-cpptools/issues/4127)
* Fix bug when attaching to an elevated process on Linux. [#4133](https://github.com/microsoft/vscode-cpptools/issues/4133)
* Fix IntelliSense-based `Go to Definition` failing for a nested class in a template class. [#4135](https://github.com/microsoft/vscode-cpptools/issues/4135)
* Fix incorrect configuration squiggles with `compilerPath` when variables are used. [#4141](https://github.com/microsoft/vscode-cpptools/issues/4141)
  * @mistersandman [PR #4142](https://github.com/microsoft/vscode-cpptools/pull/4142)
* Fix `executeReferenceProvider` when code is selected. [#4147](https://github.com/microsoft/vscode-cpptools/issues/4147)
* Fix code action for resolving missing includes via the `vcpkg` dependency manager. [PR #4156](https://github.com/microsoft/vscode-cpptools/pull/4156)

## Version 0.25.0: August 21, 2019
### New Features
* Add `Find All References`. [#15](https://github.com/microsoft/vscode-cpptools/issues/15)
* Add `-x86` options for `intelliSenseMode`. [#2275](https://github.com/microsoft/vscode-cpptools/issues/2275), [#2312](https://github.com/microsoft/vscode-cpptools/issues/2312)
* Add `c++20` option to `cppStandard`. [#3448](https://github.com/microsoft/vscode-cpptools/issues/3448)
* Add a code action for resolving missing includes via the `vcpkg` dependency manager. [PR #3791](https://github.com/microsoft/vscode-cpptools/pull/3791)

### Enhancements
* Added support for compile commands: 
  * `-iquote`. [#2088](https://github.com/microsoft/vscode-cpptools/issues/2088)
  * `-imacros`. [#2417](https://github.com/microsoft/vscode-cpptools/issues/2417)
  * `-idirafter`(`--include-directory-after` & `--include-directory-after=`). [#3713](https://github.com/microsoft/vscode-cpptools/issues/3713)
  * `-imsvc`. [#4032](https://github.com/microsoft/vscode-cpptools/issues/4032)
* Switch to using VS Code's `Go to Declaration`. [#2959](https://github.com/microsoft/vscode-cpptools/issues/2959)
* Added `compilerArgs` property setting. [PR #3950](https://github.com/microsoft/vscode-cpptools/pull/3950)
* Added support for V3 API. [PR #3987](https://github.com/microsoft/vscode-cpptools/pull/3987)
* Add `not supported` messages for ARM and Alpine containers. [PR #4027](https://github.com/microsoft/vscode-cpptools/pull/4027)
* Add validation for paths from `env` variables. [#3912](https://github.com/microsoft/vscode-cpptools/issues/3912)

### Bug Fixes
* Fix wrong type of `this` pointer. [#2303](https://github.com/microsoft/vscode-cpptools/issues/2303)
* Fix previous cache path not deleted when new cache path is specified. Note that the VS Code bug [Microsoft/vscode#59391](https://github.com/microsoft/vscode/issues/59391) still occurs on the settings UI, but this fix should delete any incomplete path names as the extension receives changes from the cache path setting. [#3644](https://github.com/microsoft/vscode-cpptools/issues/3644).
* Fix broken shell script when launch/attaching as root. [#3711](https://github.com/microsoft/vscode-cpptools/issues/3711)
  * Christian A. Jacobsen (@ChristianJacobsen) [PR MIEngine#906](https://github.com/microsoft/MIEngine/pull/906)
* Fix ".H" files not appearing in include completion results on Linux/macOS. [#3744](https://github.com/microsoft/vscode-cpptools/issues/3744)
* Fix `compile_commands.json` file changes not updated. [#3864](https://github.com/microsoft/vscode-cpptools/issues/3864).
* Fix `Failed to parse` error message in the open file scenario. [#3888](https://github.com/microsoft/vscode-cpptools/issues/3888)
* Fix loading the wrong symbols when creating or copying a file. [#3897](https://github.com/microsoft/vscode-cpptools/issues/3897)
* Fix IntelliSense process crash in clang mode. [#3898](https://github.com/microsoft/vscode-cpptools/issues/3898)
* Fix IntelliSense-based `Go to Definition` failing with `using namespace`. [#3902](https://github.com/microsoft/vscode-cpptools/issues/3902), [#4018](https://github.com/microsoft/vscode-cpptools/issues/4018)
* Fix completion not showing results for smart pointers. [#3926](https://github.com/microsoft/vscode-cpptools/issues/3926), [#3930](https://github.com/microsoft/vscode-cpptools/issues/3930)
* Fix `clang_format_path` cannot be set in workspace settings. [#3937](https://github.com/microsoft/vscode-cpptools/issues/3937)
* Fix typos and grammar in documentation.
  * @pi1024e [PR #4014](https://github.com/microsoft/vscode-cpptools/pull/4014)
* Fix NullReferenceException when unable to launch and an unresolved parameter exists in the string. This was causing a useless error message. [#4024](https://github.com/microsoft/vscode-cpptools/issues/4024), [#4090](https://github.com/microsoft/vscode-cpptools/issues/4090)
* Fix debugger can't debug file whose folder path includes a parenthesis. [#4030](https://github.com/microsoft/vscode-cpptools/issues/4030)
* Fix duplicate content appearing after formatting of a new file. [#4091](https://github.com/microsoft/vscode-cpptools/issues/4091)
* Fix `files.exclude` bug on Windows. [#4095](https://github.com/microsoft/vscode-cpptools/issues/4095)
* Fix NullReferenceException when `cwd` is null.  [MIEngine#911](https://github.com/microsoft/MIEngine/issues/911)
* Fix wrong IntelliSense for C++ types after editing within a function and after a lambda.

## Version 0.24.1: July 22, 2019
### Bug Fixes
* Fix an issue with the Outline not being populated when a file is opened. [#3877](https://github.com/microsoft/vscode-cpptools/issues/3877)
* Update scopes used by semantic colorization. [PR# 3896](https://github.com/microsoft/vscode-cpptools/pull/3896)

## Version 0.24.0: July 3, 2019
### New Features
* Semantic colorization [Documentation](https://github.com/microsoft/vscode-cpptools/blob/master/Documentation/LanguageServer/colorization.md) [#230](https://github.com/microsoft/vscode-cpptools/issues/230)
* Add `Rescan Workspace` command. [microsoft/vscode-cpptools-api#11](https://github.com/microsoft/vscode-cpptools-api/issues/11)

### Enhancements
* Configuration UI editor improvements:
  * Add list of detected compiler paths. [PR #3708](https://github.com/microsoft/vscode-cpptools/pull/3708)
  * Enable selecting/editing of other configurations and add "Advanced Settings" section. [PR #3732](https://github.com/microsoft/vscode-cpptools/pull/3732)
* Enable `envFile` for `cppdbg`. [PR #3723](https://github.com/microsoft/vscode-cpptools/pull/3723)
* Change the default path value of `C_Cpp.intelliSenseCachePath`. [#3347](https://github.com/microsoft/vscode-cpptools/issues/3347) [#3664](https://github.com/microsoft/vscode-cpptools/issues/3664)
* Change `C_Cpp.clang_format_path` to `machine` scope. [#3774](https://github.com/microsoft/vscode-cpptools/issues/3774)
* Add validation to the advanced configuration UI settings. [PR #3838](https://github.com/microsoft/vscode-cpptools/pull/3838)
* Add `Current Configuration` to `C/C++: Log Diagnostics`. [PR #3866](https://github.com/microsoft/vscode-cpptools/pull/3866)

### Bug Fixes
* Fix for gdb `follow-fork-mode` `child` not working. [#2738](https://github.com/microsoft/vscode-cpptools/issues/2738)
* Fix IntelliSense process crash on hover with certain arrays. [#3081](https://github.com/Microsoft/vscode-cpptools/issues/3081)
* Fix IntelliSense-based `Go to Definition` for goto labels. [#3111](https://github.com/microsoft/vscode-cpptools/issues/3111)
* Fix IntelliSense behaving incorrectly when files are opened with different casing on Windows. [#3229](https://github.com/microsoft/vscode-cpptools/issues/3229)
* Fix user defined literals crashing IntelliSense in clang/gcc mode. [#3481](https://github.com/microsoft/vscode-cpptools/issues/3481)
* Improve `sourceFileMap` to be more dynamic. [#3504](https://github.com/microsoft/vscode-cpptools/issues/3504)
* Fix IntelliSense-based hover document comments being shown for invalid declarations not used by the current translation unit. [#3596](https://github.com/microsoft/vscode-cpptools/issues/3596)
* Fix `Go to Definition` when is `void` missing in the parameter list of a function definition a .c file. [#3609](https://github.com/microsoft/vscode-cpptools/issues/3609)
* Fix configuration validation of compiler path and IntelliSense mode compatibility for `clang-cl.exe` compiler. [#3637](https://github.com/microsoft/vscode-cpptools/issues/3637)
* Fix resolving `${workspaceFolderBasename}` and add `${workspaceStorage}`. [#3642](https://github.com/microsoft/vscode-cpptools/issues/3642)
* Fix IntelliSense-based `Go to Definition` performance issue due to extra database iteration. [#3655](https://github.com/microsoft/vscode-cpptools/issues/3655)
* Fix `SourceRequest` causing debugging to stop with `NotImplementedException`. [#3662](https://github.com/microsoft/vscode-cpptools/issues/3662)
* Fix typo in `intelliSenseMode` description.
  * Karsten Thoms (@kthoms) [PR #3682](https://github.com/microsoft/vscode-cpptools/pull/3682)
* Fix invalid warning with typedef enums in .c files. [#3685](https://github.com/microsoft/vscode-cpptools/issues/3685)
* Fix incorrect `keyword` completion occurring for pragma `#keyword`. [#3690](https://github.com/microsoft/vscode-cpptools/issues/3690)
* Fix problem matcher to show fatal errors from GCC [#3712](https://github.com/microsoft/vscode-cpptools/issues/3712)
* Fix multi-root folders with the same name sharing the same browse database. [PR #3715](https://github.com/microsoft/vscode-cpptools/pull/3715)
* Fix `remoteProcessPicker` on Windows. [#3758](https://github.com/microsoft/vscode-cpptools/issues/3758)
* Fix crash when tag parsing Objective-C code. [#3776](https://github.com/microsoft/vscode-cpptools/issues/3776)
* Fix duplicate slashes getting added to `c_cpp_properties.json`. [PR #3778](https://github.com/microsoft/vscode-cpptools/pull/3778)
* Fix `envFile` variable substitution. [#3836](https://github.com/microsoft/vscode-cpptools/issues/3836)
* Fix missing headers popup. [PR #3840](https://github.com/microsoft/vscode-cpptools/pull/3840)
* Fix multiple anonymous unions not showing correctly in Locals while debugging. [MIEngine#820](https://github.com/microsoft/MIEngine/issues/820)
* Fix pause not working when using `DebugServer`/`MIDebuggerServerAddress` on Linux and macOS. [MIEngine#844](https://github.com/microsoft/MIEngine/issues/844)
* Improvements to CPU and memory usage when editing.

## Version 0.23.1: May 13, 2019
### Bug Fixes
* Fix `launch.json` creation when `intelliSenseEngine` is `"Disabled"`. [#3583](https://github.com/microsoft/vscode-cpptools/issues/3583)
* Fix C/C++ commands not working if the language service isn't activated. [#3615](https://github.com/microsoft/vscode-cpptools/issues/3615)
* Fix missing extension `"Details"` page. [#3621](https://github.com/microsoft/vscode-cpptools/issues/3621)
* Fix some random crashes related to IntelliSense inactive region processing.

## Version 0.23.0: May 6, 2019
### New Features
* Add a configuration UI editor to edit IntelliSense settings defined in the underlying `c_cpp_properties.json` file. [PR #3479](https://github.com/Microsoft/vscode-cpptools/pull/3479), [PR #3487](https://github.com/Microsoft/vscode-cpptools/pull/3487), [PR #3519](https://github.com/Microsoft/vscode-cpptools/pull/3519), [#3524](https://github.com/Microsoft/vscode-cpptools/issues/3524), [PR #3563](https://github.com/Microsoft/vscode-cpptools/pull/3563), [#3526](https://github.com/Microsoft/vscode-cpptools/issues/3526)
  * Add a new command `C/C++: Edit configurations (UI)` to open the UI editor.
  * Replace the `C/C++: Edit configurations...` command with `C/C++: Edit configurations (JSON)` to open `c_cpp_properties.json`.
  * The default whether to open the UI editor or JSON file is based on the `workbench.settings.editor` setting.
* Add command `C/C++: Log Diagnostics` to log language service diagnostics. [PR #3489](https://github.com/Microsoft/vscode-cpptools/pull/3489)
* Add support for `.env` files for `cppvsdbg`. [#3490](https://github.com/Microsoft/vscode-cpptools/issues/3490)

### Other Changes
* Enable flag `/permissive-` as an argument to `compilerPath` with `cl.exe`. [#1589](https://github.com/Microsoft/vscode-cpptools/issues/1589), [#3446](https://github.com/Microsoft/vscode-cpptools/issues/3446)
* Configuration squiggles for `c_cpp_properties.json` now validates if the setting values of `compilerPath` and `intelliSenseMode` match on Windows. [#2983](https://github.com/Microsoft/vscode-cpptools/issues/2983)
* Enable `-fms-extensions` to be used as an argument to `compilerPath` on Linux/Mac. [#3063](https://github.com/Microsoft/vscode-cpptools/issues/3063)
* Change the default value of `C_Cpp.intelliSenseEngineFallback` setting to `Disabled`. [#3165](https://github.com/Microsoft/vscode-cpptools/issues/3165)
* Add squiggle when `compilerPath` uses spaces and arguments without `"`. [#3357](https://github.com/Microsoft/vscode-cpptools/issues/3357)
* Change the `Disabled` value for `C_Cpp.errorSquiggles` to stop showing missing header squiggles. [#3361](https://github.com/Microsoft/vscode-cpptools/issues/3361)
* Add `enableConfigurationSquiggles` setting to allow squiggles to be disabled for `c_cpp_properties.json`. [#3403](https://github.com/Microsoft/vscode-cpptools/issues/3403)
* Switch to using the `installExtension` command for offline/insider vsix installing (to reduce install failures). [#3408](https://github.com/Microsoft/vscode-cpptools/issues/3408)
* Add a better example to the description of `C_Cpp.clang_format_style` and `C_Cpp.clang_format_fallback_style`. [#3419](https://github.com/Microsoft/vscode-cpptools/issues/3419)
* Add a new (default) value of `EnabledIfIncludesResolve` to `C_Cpp.errorSquiggles`, which only shows error squiggles if include headers are successfully resolved. [PR #3421](https://github.com/Microsoft/vscode-cpptools/pull/3421)
* Disable debug heap by default with cppvsdbg. [#3484](https://github.com/Microsoft/vscode-cpptools/issues/3484)
  * Reported by Djoulihen (@Djoulihen)
* Enable configuration squiggles for paths delimited by semicolons. [PR #3517](https://github.com/Microsoft/vscode-cpptools/pull/3517)
* Don't show release notes if the extension has never been installed before. [#3533](https://github.com/Microsoft/vscode-cpptools/issues/3533)
* Remove IntelliSense fallback code actions.

### Bug Fixes
* Fix browsing for functions with BOOST_FOREACH. [#953](https://github.com/Microsoft/vscode-cpptools/issues/953)
* Fix code action sometimes not appearing over a squiggled identifier. [#1436](https://github.com/microsoft/vscode-cpptools/issues/1436)
* Work around issue with VS Code not treating `.C` files as C++ files [Microsoft/vscode#59369](https://github.com/Microsoft/vscode/issues/59369) -- `.C` files become associated by name in `files.associations`. [#2558](https://github.com/Microsoft/vscode-cpptools/issues/2558)
* Fix various IntelliSense parsing bugs. [#2824](https://github.com/Microsoft/vscode-cpptools/issues/2824), [#3110](https://github.com/Microsoft/vscode-cpptools/issues/3110), [#3168](https://github.com/Microsoft/vscode-cpptools/issues/3168)
* Preserve newlines in documentation comments. [#2937](https://github.com/Microsoft/vscode-cpptools/issues/2937)
* Fix documentation comments above multi-line templates (and some other issues). [#3162](https://github.com/Microsoft/vscode-cpptools/issues/3162)
* Fix "Extension causes high cpu load" due to module loading. [#3213](https://github.com/Microsoft/vscode-cpptools/issues/3213)
* Fix auto-removal of compiler-provided paths in `includePath` when they end with a directory separator on Windows. [#3245](https://github.com/Microsoft/vscode-cpptools/issues/3245)
* Fix duplicate compiler build tasks appearing when `compilerPath` has arguments. [PR #3360](https://github.com/Microsoft/vscode-cpptools/pull/3360)
* Fix environment variables not resolving with `C_Cpp.intelliSenseCachePath`. [#3367](https://github.com/Microsoft/vscode-cpptools/issues/3367)
* Fix the formatting of snippets text. [#3376](https://github.com/Microsoft/vscode-cpptools/issues/3376)
* Fix the default `AccessModifierOffset` used when formatting. [#3376](https://github.com/Microsoft/vscode-cpptools/issues/3376)
* Fix null reference during initialization when using custom configuration providers. [PR #3377](https://github.com/Microsoft/vscode-cpptools/pull/3377)
* Fix symbol parsing when `__MINGW_ATTRIB_*` is used. [#3390](https://github.com/Microsoft/vscode-cpptools/issues/3390)
* Fix `compile_commands.json` configuration prompt being disabled per user instead of per folder. [PR #3399](https://github.com/Microsoft/vscode-cpptools/pull/3399)
* Fix `.cmd` and `.bat` files not working for `compilerPath` on Windows. [#3428](https://github.com/Microsoft/vscode-cpptools/issues/3428)
* Fix `compilerPath` with arguments that are surrounded by quotes. [#3428](https://github.com/Microsoft/vscode-cpptools/issues/3428)
* Fix documentation comments interpreting special characters as markdown. [#3441](https://github.com/Microsoft/vscode-cpptools/issues/3441)
* Fix hover using the configuration of the active document instead of the hovered document. [#3452](https://github.com/Microsoft/vscode-cpptools/issues/3452)
* Fix `c_cpp_properties.json` squiggles when the configuration name has regex characters. [PR #3478](https://github.com/Microsoft/vscode-cpptools/pull/3478)
* Use the `editor.tabSize` setting instead of `2` when creating build tasks. [PR #3486](https://github.com/Microsoft/vscode-cpptools/pull/3486)
* Fix some potential crashes on hover. [#3509](https://github.com/Microsoft/vscode-cpptools/issues/3509)
* Fix for `NullReferenceException` occurring when `"args"` is not specified in `launch.json`. [#3532](https://github.com/Microsoft/vscode-cpptools/issues/3532)
* Fix `Go to Definition` giving no results when IntelliSense doesn't find the symbol. [#3549](https://github.com/Microsoft/vscode-cpptools/issues/3549)
* Fix configuration squiggles with trailing backslashes. [PR #3573](https://github.com/Microsoft/vscode-cpptools/pull/3573)
* Fix `includePath` code actions, configuration prompts, and the `C/C++: Change configuration provider...` command. [PR #3576](https://github.com/Microsoft/vscode-cpptools/pull/3576)
* Fix randomly occurring crash (that could occur when opening files while IntelliSense squiggles are pending).
* Fix crash on hover (that could occur when document comments have blank lines).
* Fix icon of parameters in completion results.

## Version 0.22.1: March 21, 2019
* Fix `tasks.json` with single-line comments being overwritten when `Build and Debug Active File` is used. [#3327](https://github.com/Microsoft/vscode-cpptools/issues/3327)
* Fix an invalid `compilerPath` property getting added to `tasks.json` after doing `Configure Task` with a C/C++ compiler.
* Add IntelliSense caching for macOS 10.13 or later (0.22.0 only supported Windows and Linux).

## Version 0.22.0: March 19, 2019
### Major Changes
* Add warning squiggles for invalid properties and paths in `c_cpp_properties.json`. [#2799](https://github.com/Microsoft/vscode-cpptools/issues/2799), [PR #3283](https://github.com/Microsoft/vscode-cpptools/pull/3283)
* Add C/C++ compiler build tasks for compiling the active source file, with support for `F5` debugging and the `Build and Debug Active File` context menu command. [PR #3118](https://github.com/Microsoft/vscode-cpptools/pull/3118), [PR #3244](https://github.com/Microsoft/vscode-cpptools/pull/3244)
* Add AutoPCH support to reduce IntelliSense parsing time, with `C_Cpp.intelliSenseCachePath` and `C_Cpp.intelliSenseCacheSize` settings. It isn't enabled for Mac yet. [PR #3184](https://github.com/Microsoft/vscode-cpptools/pull/3184)

### Minor Changes
* Fix IntelliSense not working on Windows when the username has a space in it and file `C:\Users\<firstname>` exists. [#1377](https://github.com/Microsoft/vscode-cpptools/issues/1377), [#2114](https://github.com/Microsoft/vscode-cpptools/issues/2114), [#2176](https://github.com/Microsoft/vscode-cpptools/issues/2176), [#3052](https://github.com/Microsoft/vscode-cpptools/issues/3052), [#3139](https://github.com/Microsoft/vscode-cpptools/issues/3139)
* Enable `${command:cpptools.activeConfigName}` in tasks. [#1524](https://github.com/Microsoft/vscode-cpptools/issues/1524)
* Fix bugs with squiggles and IntelliSense updating after edits. [#1779](https://github.com/Microsoft/vscode-cpptools/issues/1779), [#3124](https://github.com/Microsoft/vscode-cpptools/issues/3124), [#3260](https://github.com/Microsoft/vscode-cpptools/issues/3260)
* Fix formatting (and other non-IntelliSense operations) being blocked by IntelliSense processing. [#1928](https://github.com/Microsoft/vscode-cpptools/issues/1928)
* Fix completion when the start of an identifier matches a keyword. [#1986](https://github.com/Microsoft/vscode-cpptools/issues/1986)
* Fix auto-removal of compiler-provided paths in `includePath`. [#2177](https://github.com/Microsoft/vscode-cpptools/issues/2177)
* Fix crash on Windows when 8.3 filenames are used. [#2453](https://github.com/Microsoft/vscode-cpptools/issues/2453), [#3104](https://github.com/Microsoft/vscode-cpptools/issues/3104)
* Add support for `Scope::Member` scoped symbol searches. [#2484](https://github.com/Microsoft/vscode-cpptools/issues/2484)
* Fix signature help active parameter selection when parameter names are missing or subsets of each other. [#2952](https://github.com/Microsoft/vscode-cpptools/issues/2952)
* Fix `--enable-pretty-printing` with `gdb` when complex objects are used as keys in maps. [#3024](https://github.com/Microsoft/vscode-cpptools/issues/3024)
* Fix IntelliSense-based `Go to Definition` for `noexcept` methods. [#3060](https://github.com/Microsoft/vscode-cpptools/issues/3060)
* Render macro hover expansions as C/C++. [#3075](https://github.com/Microsoft/vscode-cpptools/issues/3075)
* Enable completion after `struct` when manually invoked. [#3080](https://github.com/Microsoft/vscode-cpptools/issues/3080)
* Add `C_Cpp.suggestSnippets` setting to disable language server snippets. [#3083](https://github.com/Microsoft/vscode-cpptools/issues/3083)
* Show a prompt for changing `C_Cpp.updateChannel` to `Insiders`. [#3089](https://github.com/Microsoft/vscode-cpptools/issues/3089)
  * lh123 (@lh123) [PR #3221](https://github.com/Microsoft/vscode-cpptools/pull/3221)
* Fix `compilerPath` not getting priority over the `compile_commands.json` compiler. [#3102](https://github.com/Microsoft/vscode-cpptools/issues/3102)
* Fix Linux `compile_commands.json` compiler querying with relative paths. [#3112](https://github.com/Microsoft/vscode-cpptools/issues/3112)
* Allow `*` in `includePath` to apply to `browse.path` when `browse.path` is not specified. [#3121](https://github.com/Microsoft/vscode-cpptools/issues/3121)
  * Tucker Kern (@mill1000) [PR #3122](https://github.com/Microsoft/vscode-cpptools/pull/3122)
* Disable `(` and `<` completion commit characters. [#3127](https://github.com/Microsoft/vscode-cpptools/issues/3127)
* Add Chinese translations for command titles. [PR #3128](https://github.com/Microsoft/vscode-cpptools/pull/3128)
* Fix remote process picker bug. [#2585](https://github.com/Microsoft/vscode-cpptools/issues/2585), [#3150](https://github.com/Microsoft/vscode-cpptools/issues/3150)
* Fix command not found and empty `c_cpp_properties.json` if activation is too slow. [#3160](https://github.com/Microsoft/vscode-cpptools/issues/3160), [#3176](https://github.com/Microsoft/vscode-cpptools/issues/3176)
* Fix `cppvsdbg` debugger showing `"An unspecified error has occurred."` for structured binding variables. [#3197](https://github.com/Microsoft/vscode-cpptools/issues/3197)
* Fix bugs with the Insider reload prompt appearing when it shouldn't. [#3206](https://github.com/Microsoft/vscode-cpptools/issues/3206)
* Fix variable expansion (e.g. `${env.HOME}`) not working when `${default}` is used in `c_cpp_properties.json`. [#3309](https://github.com/Microsoft/vscode-cpptools/issues/3309)
* Fix other unreported IntelliSense engine bugs.

## Version 0.21.0: January 23, 2019
### New Features
* Add documentation comments for hover, completion, and signature help. [#399](https://github.com/Microsoft/vscode-cpptools/issues/399)
* Add completion committing for methods after `(`. [#1184](https://github.com/Microsoft/vscode-cpptools/issues/1184)
* Add macro expansions to hover. [#1734](https://github.com/Microsoft/vscode-cpptools/issues/1734)
* Add support for `__int128_t` and `__uint128_t` types. [#1815](https://github.com/Microsoft/vscode-cpptools/issues/1815)
* Add Italian translations for command titles.
  * Julien Russo (@Dotpys) [PR #2663](https://github.com/Microsoft/vscode-cpptools/pull/2663)
* Add icons for operators, structs/unions, enum values, template arguments, and macros. [#2849](https://github.com/Microsoft/vscode-cpptools/issues/2849)
* Change `#include` completion to show individual folders instead of the entire paths, fixing previous performance problems. [#2836](https://github.com/Microsoft/vscode-cpptools/issues/2836)
* Add text `(declaration)`, `(typedef)`, `(type alias)`, and `(union)` to symbols. [#2851](https://github.com/Microsoft/vscode-cpptools/issues/2851)
* Add a refresh button to the `Attach to Process` picker. [#2885](https://github.com/Microsoft/vscode-cpptools/issues/2885)
  * Matt Bise (@mbise1993) [PR #2895](https://github.com/Microsoft/vscode-cpptools/pull/2895)
* Add completion committing for templates after `<`. [#2953](https://github.com/Microsoft/vscode-cpptools/issues/2953)

### Bug Fixes
* Add the Microsoft digital signature to Windows binaries to avoid getting incorrectly flagged by virus scanners. [#1103](https://github.com/Microsoft/vscode-cpptools/issues/1103), [#2970](https://github.com/Microsoft/vscode-cpptools/issues/2970)
* Fix bugs when UTF-8 characters > 1 byte are used. [#1504](https://github.com/Microsoft/vscode-cpptools/issues/1504), [#1525](https://github.com/Microsoft/vscode-cpptools/issues/1525), [#2034](https://github.com/Microsoft/vscode-cpptools/issues/2034), [#2082](https://github.com/Microsoft/vscode-cpptools/issues/2082), [#2883](https://github.com/Microsoft/vscode-cpptools/issues/2883)
* Fix some IntelliSense process crashes. [#1785](https://github.com/Microsoft/vscode-cpptools/issues/1785), [#2913](https://github.com/Microsoft/vscode-cpptools/issues/2913)
* Fix several incorrect IntelliSense error squiggles. [#1942](https://github.com/Microsoft/vscode-cpptools/issues/1942), [#2422](https://github.com/Microsoft/vscode-cpptools/issues/2422), [#2474](https://github.com/Microsoft/vscode-cpptools/issues/2474), [#2478](https://github.com/Microsoft/vscode-cpptools/issues/2478), [#2597](https://github.com/Microsoft/vscode-cpptools/issues/2597), [#2763](https://github.com/Microsoft/vscode-cpptools/issues/2763)
* Fix some main process crashes. [#2505](https://github.com/Microsoft/vscode-cpptools/issues/2505), [#2768](https://github.com/Microsoft/vscode-cpptools/issues/2768)
* Fix incorrect IntelliSense error with Mac clang 10.0 libraries. [#2608](https://github.com/Microsoft/vscode-cpptools/issues/2608)
* Fix completion not working in template specializations. [#2620](https://github.com/Microsoft/vscode-cpptools/issues/2620)
* Fix incorrect completions after Enter is used after struct, class, etc. [#2734](https://github.com/Microsoft/vscode-cpptools/issues/2734)
* Fix memory "leak" when parsing a large workspace. [#2737](https://github.com/Microsoft/vscode-cpptools/issues/2737)
* Fix IntelliSense-based `Go to Definition` with overloads that return a template with a default param (e.g. vector) [#2736](https://github.com/Microsoft/vscode-cpptools/issues/2736)
* Fix `Go to Definition` when `__catch()`, `_NO_EXCEPT_DEBUG`, or `_LIBCPP_BEGIN_NAMESPACE_STD` is used. [#2761](https://github.com/Microsoft/vscode-cpptools/issues/2761), [#2766](https://github.com/Microsoft/vscode-cpptools/issues/2766)
* Fix `Go to Definition` when `method(void)` is used. [#2802](https://github.com/Microsoft/vscode-cpptools/issues/2802)
* Fix error `"TypeError: Cannot read property 'map' of undefined at asCompletionResult"`. [#2807](https://github.com/Microsoft/vscode-cpptools/issues/2807)
* Fix quotes around defines not supported for custom configuration providers. [#2820](https://github.com/Microsoft/vscode-cpptools/issues/2820)
* Fix PowerShell bug on Win7. [#2822](https://github.com/Microsoft/vscode-cpptools/issues/2822)
* Fix Tag Parser completion details missing keywords (i.e. `using`, `class`, `#define`, etc.). [#2850](https://github.com/Microsoft/vscode-cpptools/issues/2850)
* Fix problem with empty recursive include paths. [#2855](https://github.com/Microsoft/vscode-cpptools/issues/2855)
* Fix `NullReferenceException` on debugger launch with VS Code Insiders. [#2858](https://github.com/Microsoft/vscode-cpptools/issues/2858), [PR Microsoft/MIEngine#810](https://github.com/Microsoft/MIEngine/pull/810)
* Fix IntelliSense errors with template argument deduction. [#2907](https://github.com/Microsoft/vscode-cpptools/issues/2907), [#2912](https://github.com/Microsoft/vscode-cpptools/issues/2912)
* Retry Insider VSIX downloading with `http.proxySupport` `"off"`. [#2927](https://github.com/Microsoft/vscode-cpptools/issues/2927)
* Fix snippet completions being offered when they shouldn't be. [#2942](https://github.com/Microsoft/vscode-cpptools/issues/2942)
* Set the `editor.wordBasedSuggestions` to `false` by default to prevent incorrect completions. [#2943](https://github.com/Microsoft/vscode-cpptools/issues/2943)
* Fix IntelliSense-based `Go to Definition` for functions with function pointer parameters. [#2981](https://github.com/Microsoft/vscode-cpptools/issues/2981)
* Fix `<` incorrectly triggering completions. [#2985](https://github.com/Microsoft/vscode-cpptools/issues/2985)
* Fix recursive includes not adding paths used by `forcedInclude` files. [#2986](https://github.com/Microsoft/vscode-cpptools/issues/2986)
* Fix crash when `//` is used in a recursive `includePath`. [#2987](https://github.com/Microsoft/vscode-cpptools/issues/2987)
* Fix compiler in `compile_commands.json` not taking precedence over the `Cpp.default.compilerPath`. [#2793](https://github.com/Microsoft/vscode-cpptools/issues/2793)
* Fix `#include` completion not working for symlinks. [#2843](https://github.com/Microsoft/vscode-cpptools/issues/2843)
* Fix IntelliSense-based `Go to Definition` for `const` methods. [#3014](https://github.com/Microsoft/vscode-cpptools/issues/3014)
* Support `C_Cpp.updateChannel` for VS Code Exploration builds.

## Version 0.20.1: October 31, 2018
* Fix IntelliSense-based `Go to Declaration` when there's only a definition in a TU. [#2743](https://github.com/Microsoft/vscode-cpptools/issues/2743)
* Fix `#include` completion for standalone header files. [#2744](https://github.com/Microsoft/vscode-cpptools/issues/2744)
* Fix the highest hitting main process crash.
* Fix IntelliSense process crash with completion.

## Version 0.20.0: October 30, 2018
* Add IntegratedTerminal support for Linux and Windows. [#35](https://github.com/microsoft/vscode-cpptools/issues/35)
* Unify Visual Studio Code debug protocol parsing by using a shared library with Visual Studio.
* Fix IntelliSense-based `Go to Definition` on overloads (in the same TU). [#1071](https://github.com/Microsoft/vscode-cpptools/issues/1071)
* Fix inactive regions not being disabled when falling back to the Tag Parser. [#2181](https://github.com/Microsoft/vscode-cpptools/issues/2181)
* Fix `#include` completion not working with `compile_commands.json` or custom configuration providers. [#2242](https://github.com/Microsoft/vscode-cpptools/issues/2242)
* Fix IntelliSense failing if recursive includes removes all paths. [#2442](https://github.com/Microsoft/vscode-cpptools/issues/2442)
* Fix incorrect IntelliSense errors with MinGW (stop using `-fms-extensions` by default). [#2443](https://github.com/Microsoft/vscode-cpptools/issues/2443), [#2623](https://github.com/Microsoft/vscode-cpptools/issues/2623)
* Fix error squiggles sometimes not updating after typing. [#2448](https://github.com/Microsoft/vscode-cpptools/issues/2448)
* Add support for Mac framework paths in `compile_commands.json`. [#2508](https://github.com/Microsoft/vscode-cpptools/issues/2508)
* Fix IntelliSense-based `Go to Definition` falling back to the Tag Parser for definitions not in the TU. [#2536](https://github.com/Microsoft/vscode-cpptools/issues/2536), [#2677](https://github.com/Microsoft/vscode-cpptools/issues/2677)
* Fix IntelliSense-based `Go to Definition` on the identifier of a definition with no declaration. [#2573](https://github.com/Microsoft/vscode-cpptools/issues/2573)
* Fix IntelliSense-based `Go to Definition` not falling back to the declaration (in certain cases). [#2574](https://github.com/Microsoft/vscode-cpptools/issues/2574)
* Fix IntelliSense-based `Go to Definition` going to the wrong location after edits are made. [#2579](https://github.com/Microsoft/vscode-cpptools/issues/2579)
* Fix `Go to Definition` when the `intelliSenseEngineFallback` is `Disabled` and `#include`s are missing. [#2583](https://github.com/Microsoft/vscode-cpptools/issues/2583)
* Fix empty `C_Cpp.default.*` settings not being used. [#2584](https://github.com/Microsoft/vscode-cpptools/issues/2584)
* Fix quoting around `ssh`'s command (for the debugger). [#2585](https://github.com/Microsoft/vscode-cpptools/issues/2585)
* Fix crash on hover (and `Go to Definition`) when using the `Tag Parser`. [#2586](https://github.com/Microsoft/vscode-cpptools/issues/2586)
* Fix errors when a workspace folder isn't open. [#2613](https://github.com/Microsoft/vscode-cpptools/issues/2613), [#2691](https://github.com/Microsoft/vscode-cpptools/issues/2691)
* Fix `-isystem` without a space after getting ignored in `compile_comamands.json`. [#2629](https://github.com/Microsoft/vscode-cpptools/issues/2629)
* Fix Insiders update channel installation bugs. [#2636](https://github.com/Microsoft/vscode-cpptools/issues/2636), [#2685](https://github.com/Microsoft/vscode-cpptools/issues/2685)
* Fix IntelliSense-based `Go to Declaration` falling back to the Tag Parser if the definition is also in the TU. [#2642](https://github.com/Microsoft/vscode-cpptools/issues/2642)
* Fix the `Disabled` `intelliSenseEngine` setting not working with custom configuration providers. [#2656](https://github.com/Microsoft/vscode-cpptools/issues/2656)

## Version 0.19.0: September 27, 2018
* Change the symbol database to update without needing to save. [#202](https://github.com/Microsoft/vscode-cpptools/issues/202)
* Enable IntelliSense-based `Go to Definition` for the current translation unit, including local variables and overloaded operators. [#255](https://github.com/Microsoft/vscode-cpptools/issues/255), [#979](https://github.com/Microsoft/vscode-cpptools/issues/979)
* Improved the `Go to Definition` performance with large workspaces and files with lots of `#include`s. [#273](https://github.com/Microsoft/vscode-cpptools/issues/273)
* Disable `Go to Definition` for invalid tokens, e.g. comments, strings, keywords, etc. [#559](https://github.com/Microsoft/vscode-cpptools/issues/559)
* Add `C_Cpp.updateChannel` setting for easier access to Insider builds of the extension. [#1526](https://github.com/Microsoft/vscode-cpptools/issues/1526)
* Add support for v2 of the configuration provider API. [#2237](https://github.com/Microsoft/vscode-cpptools/issues/2237)
* Fix bug with parsing definitions in `compile_commands.json`. [#2305](https://github.com/Microsoft/vscode-cpptools/issues/2305)
* Fix `sh` failure when attaching to a remote Linux process. [#2444](https://github.com/Microsoft/vscode-cpptools/issues/2444)
* Fix incorrect default `cl.exe` macro. [PR #2468](https://github.com/Microsoft/vscode-cpptools/issues/2468)
* Fix multiple bugs with the symbols in the Outline view not updating correctly. [#2477](https://github.com/Microsoft/vscode-cpptools/issues/2477), [#2500](https://github.com/Microsoft/vscode-cpptools/issues/2500), [#2504](https://github.com/Microsoft/vscode-cpptools/issues/2504)
* Add support for `workspaceFolderBasename` expansion. [#2491](https://github.com/Microsoft/vscode-cpptools/issues/2491)
  * Gabriel Arjones (@g-arjones) [PR #2495](https://github.com/Microsoft/vscode-cpptools/pull/2495), [PR #2503](https://github.com/Microsoft/vscode-cpptools/pull/2503)
* Fix bug with variable resolution. [#2532](https://github.com/Microsoft/vscode-cpptools/issues/2532)
* Fix off-by-one bug with hover and `Go to Definition`. [#2535](https://github.com/Microsoft/vscode-cpptools/issues/2535)
* Fix [Microsoft/vscode#54213](https://github.com/Microsoft/vscode/issues/54213)

## Version 0.18.1: August 17, 2018
* Fix 0.18.0 regression causing non-MinGW compilers to use `-fms-extensions` on Windows. [#2424](https://github.com/Microsoft/vscode-cpptools/issues/2424), [#2425](https://github.com/Microsoft/vscode-cpptools/issues/2425)

## Version 0.18.0: August 17, 2018
### New Features
* Add the `C_Cpp.intelliSenseEngine` setting value of `Disabled` (for users who only use the debugger). [#785](https://github.com/Microsoft/vscode-cpptools/issues/785)
* Add `C_Cpp.workspaceSymbols` setting with default `Just My Code` to filter out system header symbols. [#1119](https://github.com/Microsoft/vscode-cpptools/issues/1119), [#2320](https://github.com/Microsoft/vscode-cpptools/issues/2320)
* Add `C_Cpp.inactiveRegionForegroundColor` and `C_Cpp.inactiveRegionBackgroundColor` settings. [#1620](https://github.com/Microsoft/vscode-cpptools/issues/1620), [#2212](https://github.com/Microsoft/vscode-cpptools/issues/2212)
  * John Patterson (@john-patterson) [PR #2308](https://github.com/Microsoft/vscode-cpptools/pull/2308)
* Add `gcc-x64` `intelliSenseMode` and send the correct clang or gcc version to our parser, fixing various IntelliSense errors. [#2112](https://github.com/Microsoft/vscode-cpptools/issues/2112), [#2175](https://github.com/Microsoft/vscode-cpptools/issues/2175), [#2260](https://github.com/Microsoft/vscode-cpptools/issues/2260), [#2299](https://github.com/Microsoft/vscode-cpptools/issues/2299), [#2317](https://github.com/Microsoft/vscode-cpptools/issues/2317)
* Make `Go to Definition` on the definition go to the declaration instead. [#2298](https://github.com/Microsoft/vscode-cpptools/issues/2298)
* Add multi-pass environment variable resolution allowing variables defined in terms of other variables. [#2057](https://github.com/Microsoft/vscode-cpptools/issues/2057)
  * John Patterson (@john-patterson) [PR #2322](https://github.com/Microsoft/vscode-cpptools/pull/2322)
* Allow users to use `~` for `${userProfile}` on Windows. [PR #2333](https://github.com/Microsoft/vscode-cpptools/pull/2333)
* Add support for compiler flags `-fms-extensions` and `-fno-ms-extensions` on Windows (the default for MinGW-based compilers). [#2363](https://github.com/Microsoft/vscode-cpptools/issues/2363)
* Make completion "show more results" (i.e. inaccessible members) when invoked a 2nd time. [#2386](https://github.com/Microsoft/vscode-cpptools/issues/2386)

### Bug Fixes
* Fix attach to process for systems without `bash` by using `sh` instead. [#569](https://github.com/Microsoft/vscode-cpptools/issues/569)
  * Andy Neff (@andyneff) [PR #2340](https://github.com/Microsoft/vscode-cpptools/pull/2340)
* Fix IntelliSense crash after hover or completion with `_Complex` types. [#689](https://github.com/Microsoft/vscode-cpptools/issues/689), [#1112](https://github.com/Microsoft/vscode-cpptools/issues/1112)
* Fix `files.exclude` not working to exclude non-workspace folders from symbol parsing. [#1066](https://github.com/Microsoft/vscode-cpptools/issues/1066)
* Fix `Switch Header/Source` to give results that match the parent folder name before using just the file name. [#1085](https://github.com/Microsoft/vscode-cpptools/issues/1085)
* Fix incorrect IntelliSense errors caused by namespace lookup failure when instantiation template arguments in clang mode. [#1395](https://github.com/Microsoft/vscode-cpptools/issues/1395), [#1559](https://github.com/Microsoft/vscode-cpptools/issues/1559), [#1753](https://github.com/Microsoft/vscode-cpptools/issues/1753), [#2272](https://github.com/Microsoft/vscode-cpptools/issues/2272)
* Fix missing parameter help when using { for constructors. [#1667](https://github.com/Microsoft/vscode-cpptools/issues/1667)
* Fix Mac framework dependencies not being discovered. [#1913](https://github.com/Microsoft/vscode-cpptools/issues/1913)
* Fix `compilerPath` not working with `${workspaceFolder}`. [#1982](https://github.com/Microsoft/vscode-cpptools/issues/1982)
* Fix red flame getting stuck after modifying `c_cpp_properties.json`. [#2077](https://github.com/Microsoft/vscode-cpptools/issues/2077)
* Don't add empty `windowsSDKVersion` if none exists. [#2300](https://github.com/Microsoft/vscode-cpptools/issues/2300)
* Fix IntelliSense crash when the gcc-8 type_traits header is used. [#2323](https://github.com/Microsoft/vscode-cpptools/issues/2323), [#2328](https://github.com/Microsoft/vscode-cpptools/issues/2328)
* Limit configuration popups to one at a time. [#2324](https://github.com/Microsoft/vscode-cpptools/issues/2324)
* Don't show `includePath` code actions if compile commands or custom configuration providers are used. [#2334](https://github.com/Microsoft/vscode-cpptools/issues/2334)
* Fix `C_Cpp.clang_format_path` not accepting environment variables. [#2344](https://github.com/Microsoft/vscode-cpptools/issues/2344)
* Fix IntelliSense not working with non-ASCII characters in the WSL install path. [#2351](https://github.com/Microsoft/vscode-cpptools/issues/2351)
* Filter out buggy IntelliSense error `"= delete" can only appear on the first declaration of a function`. [#2352](https://github.com/Microsoft/vscode-cpptools/issues/2352)
* Fix IntelliSense failing with WSL if gcc is installed bug g++ isn't. [#2360](https://github.com/Microsoft/vscode-cpptools/issues/2360)
* Fix WSL paths starting with `/mnt/` failing to get symbols parsed. [#2361](https://github.com/Microsoft/vscode-cpptools/issues/2361)
* Fix IntelliSense process crash when hovering over a designated initializer list with an anonymous struct. [#2370](https://github.com/Microsoft/vscode-cpptools/issues/2370)
* Stop showing "File: " in completion details for internal compiler defines. [#2387](https://github.com/Microsoft/vscode-cpptools/issues/2387)
* Invoke `Edit Configurations...` when the `Configuration Help` button is clicked. [#2408](https://github.com/Microsoft/vscode-cpptools/issues/2408)
* Fix provider configuration prompt not showing for newly added workspace folders. [#2415](https://github.com/Microsoft/vscode-cpptools/issues/2415)
* Fix to allow SIGINT to be sent using the kill -2 command when using pipeTransport.

## Version 0.17.7: July 22, 2018
* Fix `Go to Definition` for code scoped with an aliased namespace. [#387](https://github.com/Microsoft/vscode-cpptools/issues/387)
* Fix incorrect IntelliSense errors with template template-arguments. [#1014](https://github.com/Microsoft/vscode-cpptools/issues/1014)
* Fix crash when using designated initializer lists. [#1440](https://github.com/Microsoft/vscode-cpptools/issues/1440)
* Add `windowsSdkVersion` to `c_cpp_properties.json`. [#1585](https://github.com/Microsoft/vscode-cpptools/issues/1585)
* Add `${vcpkgRoot}` variable. [#1817](https://github.com/Microsoft/vscode-cpptools/issues/1817)
* Fix dangling IntelliSense processes. [#2075](https://github.com/Microsoft/vscode-cpptools/issues/2075), [#2169](https://github.com/Microsoft/vscode-cpptools/issues/2169)
* Fix incorrect IntelliSense errors when class template argument deduction is used. [#2101](https://github.com/Microsoft/vscode-cpptools/issues/2101)
* Skip automatic parsing of source files in Mac system framework paths. [#2156](https://github.com/Microsoft/vscode-cpptools/issues/2156)
* Fix `Edit Configurations...` not working after `c_cpp_properties.json` is deleted. [#2214](https://github.com/Microsoft/vscode-cpptools/issues/2214)
* Fix indexing of the entire root drive on Windows when no is folder open. [#2216](https://github.com/Microsoft/vscode-cpptools/issues/2216)
* Disable the config provider message for headers outside the workspace and when debugging. [#2221](https://github.com/Microsoft/vscode-cpptools/issues/2221)
* Add `Change Configuration Provider...` command. [#2224](https://github.com/Microsoft/vscode-cpptools/issues/2224)
* Fix out-of-memory crash with `#include` code actions when no folder is open. [#2225](https://github.com/Microsoft/vscode-cpptools/issues/2225)
* Fix `intelliSenseMode` with custom config providers on Windows. [#2228](https://github.com/Microsoft/vscode-cpptools/issues/2228)
* Fix formatting not working on Windows if the VC++ 2015 redist isn't installed. [#2232](https://github.com/Microsoft/vscode-cpptools/issues/2232)
* Fix variables not resolving in `macFrameworkPath`. [#2234](https://github.com/Microsoft/vscode-cpptools/issues/2234)
* Fix `Go to Definition` not working for macros followed by `.` or `->`. [#2245](https://github.com/Microsoft/vscode-cpptools/issues/2245)
* Fix `#include` autocomplete with Mac framework headers. [#2251](https://github.com/Microsoft/vscode-cpptools/issues/2251)
* Fix debugging to support empty arguments for debuggee. [#2258](https://github.com/Microsoft/vscode-cpptools/issues/2258)
* Fix `Go to Definition` bug (missing symbols outside the workspace). [#2281](https://github.com/Microsoft/vscode-cpptools/issues/2281)
* Fix incorrect hover in enum definitions. [#2286](https://github.com/Microsoft/vscode-cpptools/issues/2286)
* Add a setting to silence configuration provider warnings. [#2292](https://github.com/Microsoft/vscode-cpptools/issues/2292)
* Fix debugging async Visual C++ causing debugger to hang.
* Fix `main` snippet.

## Version 0.17.6: July 2, 2018
* Fix the database icon getting stuck with recursive includes. [#2104](https://github.com/Microsoft/vscode-cpptools/issues/2104)
* Fix the red flame appearing late with recursive includes. [#2105](https://github.com/Microsoft/vscode-cpptools/issues/2105)
* Fix source files being parsed in system directories. [#2156](https://github.com/Microsoft/vscode-cpptools/issues/2156)
* Fix internal document corruption (visible after formatting) when edits are made too soon after activation. [#2162](https://github.com/Microsoft/vscode-cpptools/issues/2162)
* Fix a crash when saving with recursive includes. [#2173](https://github.com/Microsoft/vscode-cpptools/issues/2173)
* Fix a crash when the `includePath` or `browse.path` is `"**"`. [#2174](https://github.com/Microsoft/vscode-cpptools/issues/2174)
* Fix IntelliSense for WSL without g++ installed. [#2178](https://github.com/Microsoft/vscode-cpptools/issues/2178)
* Fix random IntelliSense (completion) failures due to edits being delayed. [#2184](https://github.com/Microsoft/vscode-cpptools/issues/2184)
* Fix database deletion failure with non-ASCII file paths on Windows. [#2205](https://github.com/Microsoft/vscode-cpptools/issues/2205)
* Fix `Go to Definition` results with `var::` and `var->`, and filter out invalid constructor results. [#2207](https://github.com/Microsoft/vscode-cpptools/issues/2207)
* Fix a performance bug with recursive includes.
* Fixed a CPU usage problem on Mac related to system frameworks parsing.
* Keep the IntelliSense process around for 10 seconds after a file is closed in case it's needed again.
* Added an API so build system extensions can provide IntelliSense configurations for source files. More details at [npmjs.com](https://www.npmjs.com/package/vscode-cpptools).
* Fix automatic argument quoting when debugging with gdb/lldb to include when the argument has a '(' or ')' in it. Also escape existing '"' symbols.
* Removed `-` in `ps` call for ProcessPicker and RemoteProcessPicker. [#2183](https://github.com/Microsoft/vscode-cpptools/issues/2183)

## Version 0.17.5: June 21, 2018
* Detect `compile_commands.json` and show prompt to use it. [#1297](https://github.com/Microsoft/vscode-cpptools/issues/1297)
* Change inactive regions from gray to translucent. [#1907](https://github.com/Microsoft/vscode-cpptools/issues/1907)
* Improve performance of recursive includes paths. [#2068](https://github.com/Microsoft/vscode-cpptools/issues/2068)
* Fix IntelliSense client failure due to `No args provider`. [#1908](https://github.com/Microsoft/vscode-cpptools/issues/1908)
* Fix `#include` completion with headers in the same directory. [#2031](https://github.com/Microsoft/vscode-cpptools/issues/2031)
* Fix non-header files outside the workspace folder not being parsed (i.e. so `Go to Definition` works). [#2053](https://github.com/Microsoft/vscode-cpptools/issues/2053)
* Fix some crashes. [#2080](https://github.com/Microsoft/vscode-cpptools/issues/2080)
* Support asm clobber registers on Windows. [#2090](https://github.com/Microsoft/vscode-cpptools/issues/2090)
* Fix usage of `${config:section.setting}`. [#2165](https://github.com/Microsoft/vscode-cpptools/issues/2165)
* `browse.path` now inherits `includePath` if not set in `c_cpp_properties.json`.
* On Windows, `compilerPath` now populates with the guessed `cl.exe` path, and the `MSVC` include path is based on the `cl.exe` path.
* Fix files under a non-recursive `browse.path` being removed from the database.
* Fix `*` not working in `browse.path` with WSL.
* Fix -break-insert main returning multiple bind points. [PR Microsoft/MIEngine#729](https://github.com/Microsoft/MIEngine/pull/729)
* Use -- instead of -x for gnome-terminal. [PR Microsoft/MIEngine#733](https://github.com/Microsoft/MIEngine/pull/733)
* Added `miDebuggerArgs` in order to pass arguments to the program in `miDebuggerPath`. [PR Microsoft/MIEngine#720](https://github.com/Microsoft/MIEngine/pull/720)

## Version 0.17.4: May 31, 2018
* Fix infinite loop (caused by deadlock) when using recursive includes. [#2043](https://github.com/Microsoft/vscode-cpptools/issues/2043)
* Stop using recursive includes in the default configuration.
  * @Hyzeta [PR #2059](https://github.com/Microsoft/vscode-cpptools/pull/2059)
* Fix various other potential deadlocks and crashes.
* Fix `Go to Definition` on `#include` not filtering out results based on the path. [#1253](https://github.com/Microsoft/vscode-cpptools/issues/1253), [#2033](https://github.com/Microsoft/vscode-cpptools/issues/2033)
* Fix database icon getting stuck. [#1917](https://github.com/Microsoft/vscode-cpptools/issues/1917)

## Version 0.17.3: May 22, 2018
* Add support for `${workspaceFolder:folderName}`. [#1774](https://github.com/Microsoft/vscode-cpptools/issues/1774)
* Fix infinite loop during initialization on Windows. [#1960](https://github.com/Microsoft/vscode-cpptools/issues/1960)
* Fix main process IntelliSense-related crashes. [#2006](https://github.com/Microsoft/vscode-cpptools/issues/2006)
* Fix deadlock after formatting large files. [#2007](https://github.com/Microsoft/vscode-cpptools/issues/2007)
* Fix recursive includes failing to find some system includes. [#2019](https://github.com/Microsoft/vscode-cpptools/issues/2019)

## Version 0.17.1: May 17, 2018
* Fix IntelliSense update slowness when using recursive includes. [#1949](https://github.com/Microsoft/vscode-cpptools/issues/1949)
* Fix code navigation failure after switching between WSL and non-WSL configs. [#1958](https://github.com/Microsoft/vscode-cpptools/issues/1958)
* Fix extension crash when the `includePath` is a file or the root drive. [#1979](https://github.com/Microsoft/vscode-cpptools/issues/1979), [#1965](https://github.com/Microsoft/vscode-cpptools/issues/1965)
* Fix IntelliSense crash in `have_member_access_from_class_scope`. [#1763](https://github.com/Microsoft/vscode-cpptools/issues/1763)
* Fix `#include` completion bugs. [#1959](https://github.com/Microsoft/vscode-cpptools/issues/1959), [#1970](https://github.com/Microsoft/vscode-cpptools/issues/1970)
* Add `Debug` value for `loggingLevel` (previously the hidden value `"6"`).
* Fix C++17 features not being fully enabled with msvc-x64 mode. [#1990](https://github.com/Microsoft/vscode-cpptools/issues/1990)
* Fix IntelliSense interprocess deadlocks. [#1407](https://github.com/Microsoft/vscode-cpptools/issues/1407), [#1777](https://github.com/Microsoft/vscode-cpptools/issues/1777)

## Version 0.17.0: May 7, 2018
* Auto-complete for headers after typing `#include`. [#802](https://github.com/Microsoft/vscode-cpptools/issues/802)
* Add support for recursive `includePath`, e.g. `${workspaceFolder}/**`. [#897](https://github.com/Microsoft/vscode-cpptools/issues/897)
* Configuration improvements. [#1338](https://github.com/Microsoft/vscode-cpptools/issues/1338)
  * Potentially addresses: [#368](https://github.com/Microsoft/vscode-cpptools/issues/368), [#410](https://github.com/Microsoft/vscode-cpptools/issues/410), [#1229](https://github.com/Microsoft/vscode-cpptools/issues/1229), [#1270](https://github.com/Microsoft/vscode-cpptools/issues/1270), [#1404](https://github.com/Microsoft/vscode-cpptools/issues/1404)
* Add support for querying system includes/defines from WSL and Cygwin compilers. [#1845](https://github.com/Microsoft/vscode-cpptools/issues/1845), [#1736](https://github.com/Microsoft/vscode-cpptools/issues/1736)
* Fix IntelliSense for WSL projects in Windows builds 17110 and greater. [#1694](https://github.com/Microsoft/vscode-cpptools/issues/1694)
* Add snippets. [PR #1823](https://github.com/Microsoft/vscode-cpptools/pull/1823)
* Add support for vcpkg. [PR #1886](https://github.com/Microsoft/vscode-cpptools/pull/1886)
* Add support for custom variables in `c_cpp_properties.json` via `env`. [#1857](https://github.com/Microsoft/vscode-cpptools/issues/1857), [#368](https://github.com/Microsoft/vscode-cpptools/issues/368)
* Stop automatically adding `/usr/include` to the `includePath`. [#1819](https://github.com/Microsoft/vscode-cpptools/issues/1819)
* Fix wrong configuration being used if there are four or more. [#1599](https://github.com/Microsoft/vscode-cpptools/issues/1599)
* Fix `c_cpp_properties.json` requiring write access. [#1790](https://github.com/Microsoft/vscode-cpptools/issues/1790)
* Change file not found in `compile_commands.json` message from an error to a warning. [#1783](https://github.com/Microsoft/vscode-cpptools/issues/1783)
* Fix an IntelliSense crash during completion requests. [#1782](https://github.com/Microsoft/vscode-cpptools/issues/1782)
* Update the installed clang-format to 6.0.
* Fix bug with `compile_commands.json` when "arguments" have both a switch and a value in the arg. [#1890](https://github.com/Microsoft/vscode-cpptools/issues/1890)
* Fix bug with garbage data appearing in tooltips on Linux/Mac. [#1577](https://github.com/Microsoft/vscode-cpptools/issues/1577)

## Version 0.16.1: March 30, 2018
* Fix random deadlock caused by logging code on Linux/Mac. [#1759](https://github.com/Microsoft/vscode-cpptools/issues/1759)
* Fix compiler from `compileCommands` not being queried for includes/defines if `compilerPath` isn't set on Windows. [#1754](https://github.com/Microsoft/vscode-cpptools/issues/1754)
* Fix OSX `UseShellExecute` I/O bug. [#1756](https://github.com/Microsoft/vscode-cpptools/issues/1756)
* Invalidate partially unzipped files from package manager. [#1757](https://github.com/Microsoft/vscode-cpptools/issues/1757)

## Version 0.16.0: March 28, 2018
* Enable autocomplete for local and global scopes. [#13](https://github.com/Microsoft/vscode-cpptools/issues/13)
* Add a setting to define multiline comment patterns: `C_Cpp.commentContinuationPatterns`. [#1100](https://github.com/Microsoft/vscode-cpptools/issues/1100), [#1539](https://github.com/Microsoft/vscode-cpptools/issues/1539)
* Add a setting to disable inactive region highlighting: `C_Cpp.dimInactiveRegions`. [#1592](https://github.com/Microsoft/vscode-cpptools/issues/1592)
* Add `forcedInclude` configuration setting. [#852](https://github.com/Microsoft/vscode-cpptools/issues/852)
* Add `compilerPath`, `cStandard`, and `cppStandard` configuration settings, and query gcc/clang-based compilers for default defines. [#1293](https://github.com/Microsoft/vscode-cpptools/issues/1293), [#1251](https://github.com/Microsoft/vscode-cpptools/issues/1251), [#1448](https://github.com/Microsoft/vscode-cpptools/issues/1448), [#1465](https://github.com/Microsoft/vscode-cpptools/issues/1465), [#1484](https://github.com/Microsoft/vscode-cpptools/issues/1484)
* Fix text being temporarily gray when an inactive region is deleted. [Microsoft/vscode#44872](https://github.com/Microsoft/vscode/issues/44872)
* Add support for `${workspaceFolder}` variable in **c_cpp_properties.json**. [#1392](https://github.com/Microsoft/vscode-cpptools/issues/1392)
* Fix IntelliSense not updating in source files after dependent header files are changed. [#1501](https://github.com/Microsoft/vscode-cpptools/issues/1501)
* Change database icon to use the `statusBar.foreground` color. [#1638](https://github.com/Microsoft/vscode-cpptools/issues/1638)
* Enable C++/CLI IntelliSense mode via adding the `/clr` arg to the `compilerPath`. [#1596](https://github.com/Microsoft/vscode-cpptools/issues/1596)
* Fix delay in language service activation caused by **cpptools.json** downloading. [#1640](https://github.com/Microsoft/vscode-cpptools/issues/1640)
* Fix debugger failure when a single quote is in the path. [#1554](https://github.com/Microsoft/vscode-cpptools/issues/1554)
* Fix terminal stdout and stderr redirection to not send to VS Code. [#1348](https://github.com/Microsoft/vscode-cpptools/issues/1348)
* Fix blank config and endless "Initializing..." if the file watcher limit is hit when using `compileCommands`. [PR #1709](https://github.com/Microsoft/vscode-cpptools/pull/1709)
* Fix error squiggles re-appearing after editing then closing a file. [#1712](https://github.com/Microsoft/vscode-cpptools/issues/1712)
* Show error output from clang-format. [#1259](https://github.com/Microsoft/vscode-cpptools/issues/1259)
* Fix `add_expression_to_index` crash (most frequent crash in 0.15.0). [#1396](https://github.com/Microsoft/vscode-cpptools/issues/1396)
* Fix incorrect error squiggle `explicitly instantiated more than once`. [#871](https://github.com/Microsoft/vscode-cpptools/issues/871)

## Version 0.15.0: February 15, 2018
* Add colorization for inactive regions. [#1466](https://github.com/Microsoft/vscode-cpptools/issues/1466)
* Fix 3 highest hitting crashes. [#1137](https://github.com/Microsoft/vscode-cpptools/issues/1137), [#1337](https://github.com/Microsoft/vscode-cpptools/issues/1337), [#1497](https://github.com/Microsoft/vscode-cpptools/issues/1497)
* Update IntelliSense compiler (bug fixes and more C++17 support). [#1067](https://github.com/Microsoft/vscode-cpptools/issues/1067), [#1313](https://github.com/Microsoft/vscode-cpptools/issues/1313)
* Fix duplicate `cannot open source file` errors. [#1469](https://github.com/Microsoft/vscode-cpptools/issues/1469)
* Fix `Go to Symbol in File...` being slow for large workspaces. [#1472](https://github.com/Microsoft/vscode-cpptools/issues/1472)
* Fix stuck processes during shutdown. [#1474](https://github.com/Microsoft/vscode-cpptools/issues/1474)
* Fix error popup appearing with non-workspace files when using `compile_commands.json`. [#1475](https://github.com/Microsoft/vscode-cpptools/issues/1475)
* Fix snippet completions being blocked after `#`. [#1531](https://github.com/Microsoft/vscode-cpptools/issues/1531)
* Add more macros to `cpp.hint` (fixing missing symbols).
* Add `__CHAR_BIT__=8` to default defines on Mac. [#1510](https://github.com/Microsoft/vscode-cpptools/issues/1510)
* Added support for config variables to `c_cpp_properties.json`. [#314](https://github.com/Microsoft/vscode-cpptools/issues/314)
  * Joshua Cannon (@thejcannon) [PR #1529](https://github.com/Microsoft/vscode-cpptools/pull/1529)
* Define `_UNICODE` by default on Windows platforms. [#1538](https://github.com/Microsoft/vscode-cpptools/issues/1538)
  * Charles Milette (@sylveon) [PR #1540](https://github.com/Microsoft/vscode-cpptools/pull/1540)

## Version 0.14.6: January 17, 2018
* Fix tag parser failing (and continuing to fail after edits) when it shouldn't. [#1367](https://github.com/Microsoft/vscode-cpptools/issues/1367)
* Fix tag parser taking too long due to redundant processing. [#1288](https://github.com/Microsoft/vscode-cpptools/issues/1288)
* Fix debugging silently failing the 1st time if a C/C++ file isn't opened. [#1366](https://github.com/Microsoft/vscode-cpptools/issues/1366)
* Skip automatically adding to `files.associations` if it matches an existing glob pattern or if `C_Cpp.autoAddFileAssociations` is `false`. [#722](https://github.com/Microsoft/vscode-cpptools/issues/722)
* The debugger no longer requires an extra reload. [#1362](https://github.com/Microsoft/vscode-cpptools/issues/1362)
* Fix incorrect "Warning: Expected file ... is missing" message after installing on Linux. [#1334](https://github.com/Microsoft/vscode-cpptools/issues/1334)
* Fix "Include file not found" messages not re-appearing after settings changes. [#1363](https://github.com/Microsoft/vscode-cpptools/issues/1363)
* Performance improvements with `browse.path` parsing, and stop showing "Parsing files" when there's no actual parsing. [#1393](https://github.com/Microsoft/vscode-cpptools/issues/1393)
* Fix crash when settings with the wrong type are used. [#1396](https://github.com/Microsoft/vscode-cpptools/issues/1396)
* Allow semicolons in `browse.path`. [#1415](https://github.com/Microsoft/vscode-cpptools/issues/1415)
* Fix to handle relative pathing in source file paths properly when normalizing. [#1228](https://github.com/Microsoft/vscode-cpptools/issues/1228)
* Fix delay in language service activation caused by cpptools.json downloading. [#1429](https://github.com/Microsoft/vscode-cpptools/issues/1429)
* Add `C_Cpp.workspaceParsingPriority` setting to enable using less than 100% CPU during parsing of workspace files.
* Add `C_Cpp.exclusionPolicy` default to `checkFolders` to avoid expensive `files.exclude` checking on every file.

## Version 0.14.5: December 18, 2017
* Fix stackwalk `NullReferenceException`. [#1339](https://github.com/Microsoft/vscode-cpptools/issues/1339)
* Fix `-isystem` (or `-I`) not being used in `compile_commands.json` if there's a space after it. [#1343](https://github.com/Microsoft/vscode-cpptools/issues/1343)
* Fix header switching from `.cc` to `.hpp` files (and other cases). [#1341](https://github.com/Microsoft/vscode-cpptools/issues/1341)
* Fix reload prompts not appearing in debugging scenarios (after the initial installation). [#1344](https://github.com/Microsoft/vscode-cpptools/issues/1344)
* Add a "wait" message when commands are invoked during download/installation. [#1344](https://github.com/Microsoft/vscode-cpptools/issues/1344)
* Prevent blank "C/C++ Configuration" from appearing when debugging is started but the language service is not. [#1353](https://github.com/Microsoft/vscode-cpptools/issues/1353)

## Version 0.14.4: December 11, 2017
* Enable the language service processes to run without glibc 2.18. [#19](https://github.com/Microsoft/vscode-cpptools/issues/19)
* Enable the language service processes to run on 32-bit Linux. [#424](https://github.com/Microsoft/vscode-cpptools/issues/424)
* Fix extension process not working on Windows with non-ASCII usernames. [#1319](https://github.com/Microsoft/vscode-cpptools/issues/1319)
* Fix IntelliSense on single processor VMs. [#1321](https://github.com/Microsoft/vscode-cpptools/issues/1321)
* Enable offline installation of the extension. [#298](https://github.com/Microsoft/vscode-cpptools/issues/298)
* Add support for `-isystem` in `compile_commands.json`. [#1156](https://github.com/Microsoft/vscode-cpptools/issues/1156)
* Remember the selected configuration across launches of VS Code. [#1273](https://github.com/Microsoft/vscode-cpptools/issues/1273)
* Fix 'Add Configuration...` entries not appearing if the extension wasn't previously activated. [#1287](https://github.com/Microsoft/vscode-cpptools/issues/1287)
* Add `(declaration)` to declarations in the navigation list. [#1311](https://github.com/Microsoft/vscode-cpptools/issues/1311)
* Fix function definition body not being visible after navigation. [#1311](https://github.com/Microsoft/vscode-cpptools/issues/1311)
* Improve performance for fetching call stacks with large arguments. [#363](https://github.com/Microsoft/vscode-cpptools/issues/363)

## Version 0.14.3: November 27, 2017
* Fix disappearing parameter hints tooltip. [#1165](https://github.com/Microsoft/vscode-cpptools/issues/1165)
* Fix parameter hints only showing up after the opening parenthesis. [#902](https://github.com/Microsoft/vscode-cpptools/issues/902), [#819](https://github.com/Microsoft/vscode-cpptools/issues/819)
* Fix customer reported crashes in the TypeScript extension code. [#1240](https://github.com/Microsoft/vscode-cpptools/issues/1240), [#1245](https://github.com/Microsoft/vscode-cpptools/issues/1245)
* Fix .browse.VC-#.db files being unnecessarily created when an shm file exists. [#1234](https://github.com/Microsoft/vscode-cpptools/issues/1234)
* Fix language service to only activate after a C/C++ file is opened or a C/Cpp command is used (not onDebug).
* Fix database resetting if shutdown got blocked by an IntelliSense operation. [#1260](https://github.com/Microsoft/vscode-cpptools/issues/1260)
* Fix deadlock that can occur when switching configurations.
* Fix browse.databaseFilename changing not taking effect until a reload.

## Version 0.14.2: November 9, 2017
* Unsupported Linux clients sending excessive telemetry when the language server fails to start. [#1227](https://github.com/Microsoft/vscode-cpptools/issues/1227)

## Version 0.14.1: November 9, 2017
* Add support for multi-root workspaces. [#1070](https://github.com/Microsoft/vscode-cpptools/issues/1070)
* Fix files temporarily being unsavable after Save As and other scenarios on Windows. [Microsoft/vscode#27329](https://github.com/Microsoft/vscode/issues/27329)
* Fix files "permanently" being unsavable if the IntelliSense process launches during tag parsing of the file. [#1040](https://github.com/Microsoft/vscode-cpptools/issues/1040)
* Show pause and resume parsing commands after clicking the database icon. [#1141](https://github.com/Microsoft/vscode-cpptools/issues/1141)
* Don't show the install output unless an error occurs. [#1160](https://github.com/Microsoft/vscode-cpptools/issues/1160)
* Fix bug with `${workspaceRoot}` symbols not getting added if a parent folder is in the `browse.path`. [#1185](https://github.com/Microsoft/vscode-cpptools/issues/1185)
* Fix `Add configuration` C++ launch.json on Insiders. [#1191](https://github.com/Microsoft/vscode-cpptools/issues/1191)
* Fix extension restart logic so that the extension doesn't get stuck on "Initializing..." when it crashes. [#893](https://github.com/Microsoft/vscode-cpptools/issues/893)
* Remove the Reload window prompt after installation (it only appears if launch.json is active).
* Prevent browse database from being reset if shutdown takes > 1 second.
* Remove the `UnloadLanguageServer` command and the `clang_format_formatOnSave` setting.
* Fix bugs with include path suggestions.
* Fix max files to parse status number being too big, due to including non-`${workspaceRoot}` files.
* Update default `launch.json` configurations to use `${workspaceFolder}` instead of `${workspaceRoot}`.
* Update how default initial configurations for `launch.json` are being provided. [Microsoft/vscode#33794](https://github.com/Microsoft/vscode/issues/33794)
* Add support for normalizing source file locations. (Windows [#272](https://github.com/Microsoft/vscode-cpptools/issues/272)), (Mac OS X [#1095](https://github.com/Microsoft/vscode-cpptools/issues/1095))

## Version 0.14.0: October 19, 2017
* Add support for `compile_commands.json`. [#156](https://github.com/Microsoft/vscode-cpptools/issues/156)
* Fix crash with signature help. [#1076](https://github.com/Microsoft/vscode-cpptools/issues/1076)
* Skip parsing redundant browse.path directories. [#1106](https://github.com/Microsoft/vscode-cpptools/issues/1106)
* Fix `limitSymbolsToIncludedHeaders` not working with single files. [#1109](https://github.com/Microsoft/vscode-cpptools/issues/1109)
* Add logging to Output window. Errors will be logged by default. Verbosity is controlled by the `"C_Cpp.loggingLevel"` setting.
* Add new database status bar icon for "Indexing" or "Parsing" with progress numbers, and the previous flame icon is now just for "Updating IntelliSense".
* Stop showing `(Global Scope)` if there's actually an error in identifying the correct scope.
* Fix crash with the IntelliSense process when parsing certain template code (the most frequently hit crash).
* Fix main thread being blocked while searching for files to remove after changing `files.exclude`.
* Fix incorrect code action include path suggestion when a folder comes after "..".
* Fix a crash on shutdown.

## Version 0.13.1: October 5, 2017
* Delete unused symbol databases when `browse.databaseFilename` in `c_cpp_properties.json` changes. [#558](https://github.com/Microsoft/vscode-cpptools/issues/558)
* Fix infinite loop during IntelliSense parsing. [#981](https://github.com/Microsoft/vscode-cpptools/issues/981)
* Fix database resetting due to the extension process not shutting down fast enough. [#1060](https://github.com/Microsoft/vscode-cpptools/issues/1060)
* Fix crash with document highlighting [#1076](https://github.com/Microsoft/vscode-cpptools/issues/1076)
* Fix bug that could cause symbols to be missing when shutdown occurs during tag parsing.
* Fix bug that could cause included files to not be reparsed if they were modified after the initial parsing.
* Fix potential buffer overrun when logging is enabled.
* Add logging to help diagnose cause of document corruption after formatting.

## Version 0.13.0: September 25, 2017
* Reference highlighting is now provided by the extension for both IntelliSense engines.
* Parameter help is now provided by both IntelliSense engines.
* Light bulbs (code actions) for `#include` errors now suggest potential paths to add to the `includePath` based on a recursive search of the `browse.path`. [#846](https://github.com/Microsoft/vscode-cpptools/issues/846)
* Browse database now removes old symbols when `browse.path` changes. [#262](https://github.com/Microsoft/vscode-cpptools/issues/262)
* Add `*` on new lines after a multiline comment with `/**` is started. [#579](https://github.com/Microsoft/vscode-cpptools/issues/579)
* Fix `Go to Definition`, completion, and parameter hints for partially scoped members. [#635](https://github.com/Microsoft/vscode-cpptools/issues/635)
* Fix bug in `macFrameworkPath` not resolving variables.

## Version 0.12.4: September 12, 2017
* Fix a crash in IntelliSense for users with non-ASCII user names (Windows-only). [#910](https://github.com/Microsoft/vscode-cpptools/issues/910)
* Add `macFrameworkPath` to `c_cpp_properties.json`. [#970](https://github.com/Microsoft/vscode-cpptools/issues/970)
* Fix incorrect auto-complete suggestions when using template types with the scope operator `::`. [#988](https://github.com/Microsoft/vscode-cpptools/issues/988)
* Fix potential config file parsing failure. [#989](https://github.com/Microsoft/vscode-cpptools/issues/989)
* Support `${env:VAR}` syntax for environment variables in `c_cpp_properties.json`. [#1000](https://github.com/Microsoft/vscode-cpptools/issues/1000)
* Support semicolon delimiters for include paths in `c_cpp_properties.json` to better support environment variables. [#1001](https://github.com/Microsoft/vscode-cpptools/issues/1001)
* Add `__LITTLE_ENDIAN__=1` to default defines so that "endian.h" is not needed on Mac projects. [#1005](https://github.com/Microsoft/vscode-cpptools/issues/1005)
* Fix source code files on Windows with incorrect casing. [#984](https://github.com/Microsoft/vscode-cpptools/issues/984)

## Version 0.12.3: August 17, 2017
* Fix regression for paths containing multibyte characters. [#958](https://github.com/Microsoft/vscode-cpptools/issues/958)
* Fix bug with the Tag Parser completion missing results. [#943](https://github.com/Microsoft/vscode-cpptools/issues/943)
* Add /usr/include/machine or i386 to the default Mac `includePath`. [#944](https://github.com/Microsoft/vscode-cpptools/issues/944)
* Add a command to reset the Tag Parser database. [#601](https://github.com/Microsoft/vscode-cpptools/issues/601), [#464](https://github.com/Microsoft/vscode-cpptools/issues/464)
* Fix bug with error-related code actions remaining after the errors are cleared.
* Fix bug with Tag Parser completion not working when :: preceded an identifier.
* Upgrade SQLite (for better reliability and performance).

## Version 0.12.2: August 2, 2017
* Fix bug in our build system causing Windows binaries to build against the wrong version of the Windows SDK. [#325](https://github.com/Microsoft/vscode-cpptools/issues/325)
* Added a gcc problemMatcher. [#854](https://github.com/Microsoft/vscode-cpptools/issues/854)
* Fix bug where .c/.cpp files could get added to `files.associations` as the opposite "cpp"/"c" language after `Go to Definition` on a symbol. [#884](https://github.com/Microsoft/vscode-cpptools/issues/884)
* Remove completion results after `#pragma`. [#886](https://github.com/Microsoft/vscode-cpptools/issues/886)
* Fix a possible infinite loop when viewing Boost sources. [#888](https://github.com/Microsoft/vscode-cpptools/issues/888)
* Fix `Go to Definition` not working for files in `#include_next`. [#906](https://github.com/Microsoft/vscode-cpptools/issues/906)
  * Also fix incorrect preprocessor suggestions at the end of a `#include_next`.
* Skip automatically adding to `files.associations` if they already match global patterns. [Microsoft/vscode#27404](https://github.com/Microsoft/vscode/issues/27404)
* Fix a crash with the IntelliSense process (responsible for ~25% of all crashes).

## Version 0.12.1: July 18, 2017
* Fix Tag Parser features not working with some MinGW library code.
* Fix a symbol search crash.
* Fix an IntelliSense engine compiler crash.
* Fix `Go to Declaration` to return `Go to Definition` results if the declarations have no results.
* Fix formatting with non-ASCII characters in the path. [#870](https://github.com/Microsoft/vscode-cpptools/issues/870)
* Fix handling of symbolic links to files on Linux/Mac. [#872](https://github.com/Microsoft/vscode-cpptools/issues/872)
* Move red flame icon to its own section so the configuration text is always readable. [#875](https://github.com/Microsoft/vscode-cpptools/issues/875)
* Remove `addWorkspaceRootToIncludePath` setting and instead make `${workspaceRoot}` in `browse.path` explicit.
* Add `Show Release Notes` command.
* Add `Edit Configurations...` command to the `Select a Configuration...` dropdown.
* Update Microsoft Visual C++ debugger to Visual Studio 2017 released components.
  * Fix issue with showing wrong thread. [#550](https://github.com/Microsoft/vscode-cpptools/issues/550)
  * Fix issue with binaries compiled with /FASTLINK causing debugger to hang. [#484](https://github.com/Microsoft/vscode-cpptools/issues/484)
* Fix issue in MinGW/Cygwin debugging where stop debugging causes VS Code to hang. [PR Microsoft/MIEngine#636](https://github.com/Microsoft/MIEngine/pull/636)

## Version 0.12.0: June 26, 2017
* The default IntelliSense engine now provides semantic-aware autocomplete suggestions for `.`, `->`, and `::` operators. [#13](https://github.com/Microsoft/vscode-cpptools/issues/13)
* The default IntelliSense engine now reports the unresolved include files in referenced headers and falls back to the Tag Parser until headers are resolved.
  * This behavior can be overridden by setting `"C_Cpp.intelliSenseEngineFallback": "Disabled"`
* Added `"intelliSenseMode"` property to `c_cpp_properties.json` to allow switching between MSVC and Clang modes. [#710](https://github.com/Microsoft/vscode-cpptools/issues/710), [#757](https://github.com/Microsoft/vscode-cpptools/issues/757)
* A crashed IntelliSense engine no longer gives the popup message, and it automatically restarts after an edit to the translation unit occurs.
* Fix the IntelliSense engine to use "c" mode if a C header is opened before the C file.
* Fix a bug which could cause the IntelliSense engine to not update results if changes are made to multiple files of a translation unit.
* Auto `files.association` registers "c" language headers when `Go to Definition` is used in a C file.
* Downloading extension dependencies will retry up to 5 times in the event of a failure. [#694](https://github.com/Microsoft/vscode-cpptools/issues/694)
* Changes to `c_cpp_properties.json` are detected even if file watchers fail.
* Update default IntelliSense options for MSVC mode to make Boost projects work better. [#775](https://github.com/Microsoft/vscode-cpptools/issues/775)
* Fix `Go to Definition` not working until all `browse.path` files are re-scanned. [#788](https://github.com/Microsoft/vscode-cpptools/issues/788)

## Version 0.11.4: June 2, 2017
* Fix `System.Xml.Serialization.XmlSerializationReader threw an exception` when debugging on Linux. [#792](https://github.com/Microsoft/vscode-cpptools/issues/792)
* Fix escaping for `${workspaceRoot}` in `launch.json`.

## Version 0.11.3: May 31, 2017
* Fix `x86_64-pc-linux-gnu` and `x86_64-linux-gnu` paths missing from the default `includePath`.

## Version 0.11.2: May 24, 2017
* Revert the default `C_Cpp.intelliSenseEngine` setting back to "Tag Parser" for non-Insiders while we work on improving the migration experience.

## Version 0.11.1: May 19, 2017
* Add keywords to auto-complete (C, C++, or preprocessor). [#120](https://github.com/Microsoft/vscode-cpptools/issues/120)
* Fix non-recursive `browse.path` on Linux/Mac. [#546](https://github.com/Microsoft/vscode-cpptools/issues/546)
* Fix .clang-format file not being used on Linux/Mac. [#604](https://github.com/Microsoft/vscode-cpptools/issues/604)
* Stop setting the c/cpp `editor.quickSuggestions` to false. [#606](https://github.com/Microsoft/vscode-cpptools/issues/606)
  * We also do a one-time clearing of that user setting, which will also copy any other c/cpp workspace settings to user settings. The workspace setting isn't cleared.
* Fix selection range off by one with `Peek Definition`. [#648](https://github.com/Microsoft/vscode-cpptools/issues/648)
* Upgrade the installed clang-format to 4.0 [#656](https://github.com/Microsoft/vscode-cpptools/issues/656)
* Make keyboard shortcuts only apply to c/cpp files. [#662](https://github.com/Microsoft/vscode-cpptools/issues/662)
* Fix autocomplete with qstring.h. [#666](https://github.com/Microsoft/vscode-cpptools/issues/666)
* Fix C files without a ".c" extension from being treated like C++ for `errorSquiggles`. [#673](https://github.com/Microsoft/vscode-cpptools/issues/673)
* Make the C IntelliSense engine use C11 instead of C89. [#685](https://github.com/Microsoft/vscode-cpptools/issues/685)
* Fix bug with clang-format not working with non-trimmed styles. [#691](https://github.com/Microsoft/vscode-cpptools/issues/691)
* Enable the C++ IntelliSense engine to use six C++17 features. [#699](https://github.com/Microsoft/vscode-cpptools/issues/699)
* Add reload prompt when a settings change requires it.
* Prevent non-existent files from being returned in `Go To Definition` results.

## Version 0.11.0: April 24, 2017
* Enabled first IntelliSense features based on the MSVC engine.
  * Quick info tooltips and compiler errors are provided by the MSVC engine.
  * `C_Cpp.intelliSenseEngine` property controls whether the new engine is used or not.
  * `C_Cpp.errorSquiggles` property controls whether compiler errors are made visible in the editor.
* Add `Go to Declaration` and `Peek Declaration`. [#271](https://github.com/Microsoft/vscode-cpptools/issues/271)
* Fix language-specific workspace settings leaking into user settings. [Microsoft/vscode#23118](https://github.com/Microsoft/vscode/issues/23118)
* Fix `files.exclude` not being used in some cases. [#485](https://github.com/Microsoft/vscode-cpptools/issues/485)
* Fix a couple potential references to an undefined `textEditor`. [#584](https://github.com/Microsoft/vscode-cpptools/issues/584)
* Move changes from `README.md` to `CHANGELOG.md`. [#586](https://github.com/Microsoft/vscode-cpptools/issues/586)
* Fix crash on Mac/Linux when building the browse database and `nftw` fails. [#591](https://github.com/Microsoft/vscode-cpptools/issues/591)
* Add `Alt+N` keyboard shortcut for navigation. [#593](https://github.com/Microsoft/vscode-cpptools/issues/593)
* Fix autocomplete crash when the result has an invalid UTF-8 character. [#608](https://github.com/Microsoft/vscode-cpptools/issues/608)
* Fix symbol search crash with `_` symbol. [#611](https://github.com/Microsoft/vscode-cpptools/issues/611)
* Fix the `Edit Configurations` command when '#' is in the workspace root path. [#625](https://github.com/Microsoft/vscode-cpptools/issues/625)
* Fix clang-format `TabWidth` not being set when formatting with the `Visual Studio` style. [#630](https://github.com/Microsoft/vscode-cpptools/issues/630)
* Enable `clang_format_fallbackStyle` to be a custom style. [#641](https://github.com/Microsoft/vscode-cpptools/issues/641)
* Fix potential `undefined` references when attaching to a process. [#650](https://github.com/Microsoft/vscode-cpptools/issues/650)
* Fix `files.exclude` not working on Mac. [#653](https://github.com/Microsoft/vscode-cpptools/issues/653)
* Fix crashes during edit and hover with unexpected UTF-8 data. [#654](https://github.com/Microsoft/vscode-cpptools/issues/654)

## Version 0.10.5: March 21, 2017
* Fix a crash that randomly occurred when the size of a document increased. [#430](https://github.com/Microsoft/vscode-cpptools/issues/430)
* Fix browsing not working for Linux/Mac stdlib.h functions. [#578](https://github.com/Microsoft/vscode-cpptools/issues/578)
* Additional fixes for switch header/source not respecting `files.exclude`. [#485](https://github.com/Microsoft/vscode-cpptools/issues/485)
* Made `editor.quickSuggestions` dependent on `C_Cpp.autocomplete`. [#572](https://github.com/Microsoft/vscode-cpptools/issues/572)
  * We recommend you close and reopen your settings.json file anytime you change the `C_Cpp.autocomplete` setting. [More info here](https://github.com/Microsoft/vscode-cpptools/releases).

## Version 0.10.4: March 15, 2017
* Fix a crash in signature help. [#525](https://github.com/microsoft/vscode-cpptools/issues/525)
* Re-enable switch header/source when no workspace folder is open. [#541](https://github.com/microsoft/vscode-cpptools/issues/541)
* Fix inline `clang_format_style`. [#536](https://github.com/microsoft/vscode-cpptools/issues/536)
* Some other minor bug fixes.

## Version 0.10.3: March 7, 2017
* Database stability fixes.
* Added enums to the C_Cpp settings so the possible values are displayed in the dropdown.
* Change from `${command.*}` to `${command:*}`. [#521](https://github.com/Microsoft/vscode-cpptools/issues/521)
* Current execution row was not highlighting in debug mode when using gdb. [#526](https://github.com/microsoft/vscode-cpptools/issues/526)

## Version 0.10.2: March 1, 2017
* New `addWorkspaceRootToIncludePath` setting allows users to disable automatic parsing of all files under the workspace root. [#374](https://github.com/Microsoft/vscode-cpptools/issues/374)
* The cpp.hint file was missing from the vsix package. [#508](https://github.com/Microsoft/vscode-cpptools/issues/508)
* Switch header/source now respects `files.exclude`. [#485](https://github.com/Microsoft/vscode-cpptools/issues/485)
* Switch header/source performance improvements. [#231](https://github.com/Microsoft/vscode-cpptools/issues/231)
* Switch header/source now appears in the right-click menu.
* Improvements to signature help.
* Various other bug fixes.

## Version 0.10.1: February 9, 2017
* Bug fixes.

## Version 0.10.0: January 24, 2017
* Suppressed C++ language auto-completion inside a C++ comment or string literal. TextMate based completion is still available.
* Fixed bugs regarding the filtering of files and symbols, including:
  * Find-symbol now excludes symbols found in `files.exclude` or `search.exclude` files
  * Go-to-definition now excludes symbols found in `files.exclude` files (i.e. `search.exclude` paths are still included).
* Added option to disable `clang-format`-based formatting provided by this extension via `"C_Cpp.formatting" : "disabled"`
* Added new `pipeTransport` functionality within the `launch.json` to support pipe communications with `gdb/lldb` such as using `plink.exe` or `ssh`.
* Added support for `{command.pickRemoteProcess}` to allow picking of processes for remote pipe connections during `attach` scenarios. This is similar to how `{command.pickProcess}` works for local attach.
* Bug fixes.

## Version 0.9.3: December 8, 2016
* [December update](https://aka.ms/cppvscodedec) for C/C++ extension
* Ability to map source files during debugging using `sourceFileMap` property in `launch.json`.
* Enable pretty-printing by default for gdb users in `launch.json`.
* Bug fixes.

## Version 0.9.2: September 22, 2016
* Bug fixes.

## Version 0.9.1: September 7, 2016
* Bug fixes.

## Version 0.9.0: August 29, 2016
* [August update](https://blogs.msdn.microsoft.com/vcblog/2016/08/29/august-update-for-the-visual-studio-code-cc-extension/) for C/C++ extension.
* Debugging for Visual C++ applications on Windows (Program Database files) is now available.
* `clang-format` is now automatically installed as a part of the extension and formats code as you type.
* `clang-format` options have been moved from c_cpp_properties.json file to settings.json (File->Preferences->User settings).
* `clang-format` fallback style is now set to 'Visual Studio'.
* Attach now requires a request type of `attach` instead of `launch`.
* Support for additional console logging using the keyword `logging` inside `launch.json`.
* Bug fixes.

## Version 0.8.1: July 27, 2016
* Bug fixes.

## Version 0.8.0: July 21, 2016
* [July update](https://blogs.msdn.microsoft.com/vcblog/2016/07/26/july-update-for-the-visual-studio-code-cc-extension/) for C/C++ extension.
* Support for debugging on OS X with LLDB 3.8.0. LLDB is now the default debugging option on OS X.
* Attach to process displays a list of available processes.
* Set variable values through Visual Studio Code's locals window.
* Bug fixes.

## Version 0.7.1: June 27, 2016
* Bug fixes.

## Version 0.7.0: June 20, 2016
* [June Update](https://blogs.msdn.microsoft.com/vcblog/2016/06/01/may-update-for-the-cc-extension-in-visual-studio-code/) for C/C++ extension.
* Bug fixes.
* Switch between header and source.
* Control which files are processed under include path.

## Version 0.6.1: June 3, 2016
* Bug fixes.

## Version 0.6.0: May 24, 2016
* [May update](https://blogs.msdn.microsoft.com/vcblog/2016/07/26/july-update-for-the-visual-studio-code-cc-extension/) for C/C++ extension.
* Support for debugging on OS X with GDB.
* Support for debugging with GDB on MinGW.
* Support for debugging with GDB on Cygwin.
* Debugging on 32-bit Linux now enabled.
* Format code using clang-format.
* Experimental fuzzy auto-completion.
* Bug fixes.

## Version 0.5.0: April 14, 2016
* Usability and correctness bug fixes.
* Simplify installation experience.
* Usability and correctness bug fixes.

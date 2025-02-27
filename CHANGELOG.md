# Changelog

All notable changes to this project will be documented in this file.

This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Changed
- Automatically restart Dock.app after installing the scripting-addition, and tweak messages shown when a payload gets loaded, is already loaded or does not support the version of macOS it's running on [#135](https://github.com/koekeishiya/yabai/issues/135)
- Work around macOS craziness so that we can properly tile a window after it leaves native fullscreen mode [#36](https://github.com/koekeishiya/yabai/issues/36)

## [1.1.2] - 2019-07-15
### Changed
- Float native macOS fullscreen spaces [#130](https://github.com/koekeishiya/yabai/issues/130)
- Write error messsages returned to the client through *stderr* [#131](https://github.com/koekeishiya/yabai/issues/131)
- Allow window focus command to work without the existence of a focused window [#133](https://github.com/koekeishiya/yabai/issues/133)

## [1.1.1] - 2019-07-14
### Changed
- The status bar should be disabled by default, if setting is missing from the config [#126](https://github.com/koekeishiya/yabai/issues/126)

## [1.1.0] - 2019-07-14
### Added
- Make loading scripting-addition more robust - validating version and functionality [#108](https://github.com/koekeishiya/yabai/issues/108)
- Merge options for query constraints with command selectors to have a unified method for addressing displays, spaces, and windows,
  as well as allowing commands to specify both a *selected* and a *given entity* of its type [#112](https://github.com/koekeishiya/yabai/issues/112)

### Changed
- Dragging a tiled window to another display using the mouse will cause the window to be warped to that display upon release [#103](https://github.com/koekeishiya/yabai/issues/103)
- Escape quotes in window titles returned through query commands [#114](https://github.com/koekeishiya/yabai/issues/114)
- Extend window, space and display properties exposed through *query* commands [#116](https://github.com/koekeishiya/yabai/issues/116)
- Native macOS fullscreen spaces can now be addressed using their mission-control index, and can also be moved [#117](https://github.com/koekeishiya/yabai/issues/117)
- Opacity changes only apply to windows that properly identify as  "standard" or "dialog" windows [#120](https://github.com/koekeishiya/yabai/issues/120)
- The status bar should now properly draw above any potential window that overlaps its frame [#124](https://github.com/koekeishiya/yabai/issues/124)
- Support *XDG_CONFIG_HOME* when locating the config file [#125](https://github.com/koekeishiya/yabai/issues/125)
- Allow every single config setting to be applied at runtime with immediate effect. Run config asynchronously after initialization [#122](https://github.com/koekeishiya/yabai/issues/122)

## [1.0.6] - 2019-07-09
### Changed
- No longer necessary to depend on the scripting-addition to focus a window [#102](https://github.com/koekeishiya/yabai/issues/102)
- Extend definition of *WINDOW_SEL* to include *smallest* and *largest* [#105](https://github.com/koekeishiya/yabai/issues/105)

## [1.0.5] - 2019-07-07
### Changed
- Fix missing quotation of string value outputted through *window query* commands [#90](https://github.com/koekeishiya/yabai/issues/90)

## [1.0.4] - 2019-07-06
### Changed
- Fixed an issue that prevented *yabai* from running under multiple users simultaneously [#95](https://github.com/koekeishiya/yabai/issues/95)
- Extend window properties exposed through *query* commands [#90](https://github.com/koekeishiya/yabai/issues/90)
- Extend definition of *WINDOW_SEL*, *SPACE_SEL* and *DISPLAY_SEL* to include *first*, *last*, and *recent* [#85](https://github.com/koekeishiya/yabai/issues/85)

## [1.0.3] - 2019-06-30
### Changed
- Prevent *status_bar* and *window borders* from displaying in native fullscreen spaces [#71](https://github.com/koekeishiya/yabai/issues/71)
- Fixed an issue with the *status_bar* where *has_battery* and *charging* would not be default initialized when macOS report that there are zero power sources [#60](https://github.com/koekeishiya/yabai/issues/60)
- Properly destroy the underlaying *view* when a *space* changes layout [#81](https://github.com/koekeishiya/yabai/issues/81)

## [1.0.2] - 2019-06-25
### Changed
- Hide power indicator from the status-bar if a battery could not be found [#60](https://github.com/koekeishiya/yabai/issues/60)
- Disable focus follows mouse while the *mouse_modifier* key is held down [#62](https://github.com/koekeishiya/yabai/issues/62)
- Silence meaningless warning reported by the scripting-bridge framework [#55](https://github.com/koekeishiya/yabai/issues/55)
- Extend definition of *WINDOW_SEL* to include *mouse*, targetting the window below the cursor [#66](https://github.com/koekeishiya/yabai/issues/66)
- Allow all *config* (except *status_bar*) settings to be edited at runtime [#69](https://github.com/koekeishiya/yabai/issues/69)
- Window should not be added to the window-tree twice when deminimized on an inactive display [#70](https://github.com/koekeishiya/yabai/issues/70)
- Expose *window_placement* as a config setting to specify if windows become the first or second child [#65](https://github.com/koekeishiya/yabai/issues/65)

## [1.0.1] - 2019-06-23
### Added
- First official release

[Unreleased]: https://github.com/koekeishiya/yabai/compare/v1.1.2...HEAD
[1.1.2]: https://github.com/koekeishiya/yabai/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/koekeishiya/yabai/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/koekeishiya/yabai/compare/v1.0.6...v1.1.0
[1.0.6]: https://github.com/koekeishiya/yabai/compare/v1.0.5...v1.0.6
[1.0.5]: https://github.com/koekeishiya/yabai/compare/v1.0.4...v1.0.5
[1.0.4]: https://github.com/koekeishiya/yabai/compare/v1.0.3...v1.0.4
[1.0.3]: https://github.com/koekeishiya/yabai/compare/v1.0.2...v1.0.3
[1.0.2]: https://github.com/koekeishiya/yabai/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/koekeishiya/yabai/releases/tag/v1.0.1

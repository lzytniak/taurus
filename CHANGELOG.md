# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).
This file follows the formats and conventions from [keepachangelog.com]

Note: changes in the [support-3.x] branch (which was split from 
the master branch after [3.7.1] and maintained in parallel to the 
develop branch)  won't be reflected in this file. 

## [Unreleased]


## [4.0.1] - 2016-07-19
Jul16 milestone. 
First release of the Taurus 4 series.
Largely (but not 100%) compatible with taurus 3 series.
For a full log of commits since Jan16, run (in your git repo):
`git log 3.7.0..4.0.1` 

### Added
- Quantities (units) support ([TEP14])
- Scheme-agnostic core helpers ([TEP3])
- Model fragment support ([TEP14])
- PyQt new-style signals support (#187)
- support for guiqwt >= 3 (#270)
- New icon API (taurus.qt.qtgui.icon) (#280) 
- New `taurusiconcatalog` application (#280)
- Backwards compatibility layer for migration from Taurus 3.x ([TEP14])
- New deprecation API (`Logger.deprecated` and `deprecation_decorator`)
- new unit tests (from ~50 to ~550 unit tests)
- This CHANGELOG.md file

### Changed
- Tango dependency is now **optional** ([TEP3])
- Improved and simplified core API ([TEP3], [TEP14]):
    - Configuration and Attribute Models are now merged into Attribute
    - Taurus model base classes are now scheme-agnostic
    - Improved model name validators (enforcing RFC3986 -compliant model 
    names)
- Eval scheme improved (more natural and powerful syntax) ([TEP14])
- Epics scheme plugin improved (and is now installed) (#215)
- Improved installation and distribution scripts (now using setuptools),
(#279)
- Improved testsuite (new `taurustestsuite` command allowing regexp 
exclusions)
- Improved Icon Theme support (also for windows)
- taurus.qt now depends on PyQt>=4.8 (before was 4.4)
- taurus.qt.qtgui.extra_nexus now depends on PyMca5 (before was 4.7)
- Updated documentation (#221)

### Deprecated
- Support for old-style signals
- Support for PyQt API1
- Taurus3.x tango-centric API (see [TEP3], [TEP14])
- old-style tango and eval model names (non-RFC3986 compliant)
- taurus.qt.qtgui.resource module
- taurus.external.ordereddict

### Removed
- Deprecated modules (see #234 for details & replacements)
    - taurus.core.utils
    - taurus.core.util.decorator.deprecated
    - taurus.qt.qtgui.table.taurusvaluestable_ro
    - taurus.qt.qtgui.panel.taurusattributechooser
    - taurus.qt.qtgui.panel.taurusconfigbrowser
    - taurus.qt.qtgui.base.taurusqattribute
    - taurus.qt.gtgui.extra_xterm
    - taurus.qt.gtgui.extra_pool
    - taurus.qt.gtgui.extra_macroexecutor
    - taurus.qt.gtgui.extra_sardana
    - taurus.qt.gtgui.gauge
    - taurus.qt.qtgui.image
    - taurus.qt.qtopengl
    - taurus.qt.uic
    - taurus.web
- `spec` scheme plugin (#216)
- `sim` scheme plugin (#217)
- Obsolete `setup.py` commands (`build_resources`, `build_doc`,...) 
(#279)
- Icon resource files (but the icons are still available and accessible)
(#280)

### Fixed
- Installation now possible with pip (no need of --egg workaround)
- Documentation generation issues (#288, #273, #221)
- Several bugs and feature-req in TaurusTrend2D 
- Issues in TaurusArrayEditor (#260, #261) 
- TaurusTrend Export to ASCII issues (#300, #277, #253)
- `resource` scheme plugin (#218)
- windows installer (#278)
- [Many other issues](https://sf.net/p/tauruslib/tickets/milestone/Jul16/)


## [3.7.1] - 2016-03-17
Hotfix for RTD (no library changes)

### Fixed
- RTD issue (bug 273)  


## [3.7.0] - 2016-02-17 
Jan16 milestone. 
For a full log of commits since Jul15, run (in your git repo):
`git log 3.6.0..3.7.0` 

### Added
- Support for sqlite DB in Tango (ticket #148)

### Fixed
- Many usability bugs in TaurusTrend2D and other
  guiqwt-based widgets (#238, #240, #244, #247, #251, #258)
- Issues with "export to ASCII" feature of plots
- Issues with PLY optimization (#262)
- "taurus-polling-period" argument works for evaluation
  attributes now too (#249)
- [Many other issues](http://sf.net/p/tauruslib/tickets/milestone/Jan16/)
    

## [3.6.1] - 2015-10-01
Hotfix for docs (no library changes)

### Fixed
- documentation issues (#181, #191, #194)


## [3.6.0] - 2015-07-22 
Jul15 milestone. 
For a full log of commits since Jan15, run (in your git repo):
`git log 3.4.0..3.6.0` 

### Added
- support of user creation/removal of custom external application
launchers at run time (see #158)
- support of LimaCCDs DS (see #175) and improvements in the codecs

### Changed
- taurusplot/trend uses the same order than the legend for exported
data (see #161)
- Docs: several improvements and made ReadTheDocs-compliant

### Fixed
- Fixed memory leaks in plots/trends (see #171)
- [fixed many bugs in TaurusPlot,  TaurusWheel,  TaurusImageDialog,
and several other places](https://sf.net/p/tauruslib/tickets/milestone/Jul15/)



[keepachangelog.com]: http://keepachangelog.com
[TEP3]: https://sf.net/p/tauruslib/wiki/TEP3/
[TEP14]: https://sf.net/p/tauruslib/wiki/TEP14/
[Unreleased]: https://sf.net/p/tauruslib/taurus.git/ci/develop/tree/
[4.0.1]: https://sf.net/p/tauruslib/taurus.git/ci/4.0.0/tree/
[3.7.1]: https://sf.net/p/tauruslib/taurus.git/ci/3.7.1/tree/
[3.7.0]: https://sf.net/p/tauruslib/taurus.git/ci/3.7.0/tree/
[3.6.0]: https://sf.net/p/tauruslib/taurus.git/ci/3.6.0/tree/
[support-3.x]: https://sf.net/p/tauruslib/taurus.git/ci/support-3.x/tree/




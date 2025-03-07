# Changelog

## [1.0.2] - 2022-03-18

### Fixed
* [#675](https://github.com/plotly/dash-bio/pull/675) Fixed an issue with the JS resource files in the npm release of dash-bio. As pointed out in [this community post](https://community.plotly.com/t/unable-to-use-dash-bio-for-plotting-ideograms-due-to-incorrect-javascript-dependency/61939/5) some of the dependencies have not been resolved at their external `unpkg` URL.
* [#671](https://github.com/plotly/dash-bio/pull/671) Fixed Onco-Print range property description.


## [1.0.1] - 2022-01-19

### Changed
* [#667](https://github.com/plotly/dash-bio/pull/667) Added support for dash-bio-utils stub package and deprecation warning.
* [#667](https://github.com/plotly/dash-bio/pull/667) Updated Ideogram version, props and removed support for old versions of ideogram (for more info see [#393](https://github.com/plotly/dash-bio/pull/393)).


## [1.0.0] - 2022-01-17

### Changed
* [#589](https://github.com/plotly/dash-bio/pull/593) Merged dash-bio-utils into the dash bio package namespace.

### Fixed
* [#646](https://github.com/plotly/dash-bio/pull/646) Fixed dendrogram domain whitespaces for Clustergram when dendrogram property is not set for either axis (for more info see [#644](https://github.com/plotly/dash-bio/issues/644)).

## [0.9.0] - 2021-12-14

### Fixed
* [#629](https://github.com/plotly/dash-bio/pull/629) Fixed an issue where IGV would generate duplicate tracks in the browser when a reload of the module was triggered through dcc.Tabs (for more info see [#572](https://github.com/plotly/dash-bio/issues/572)).

### Added
* [#587](https://github.com/plotly/dash-bio/pull/587) Added JSME component.
* [#628](https://github.com/plotly/dash-bio/pull/628) Added option to add colored labels to rows and columns on Clustergram.
* [#640](https://github.com/plotly/dash-bio/pull/640) Added loading states to each component to support custom loading css with `dash-data-is-loading`.
* [#642](https://github.com/plotly/dash-bio/pull/642) Added `scrollZoom` property to Molecule2dViewer.
* [#641](https://github.com/plotly/dash-bio/pull/641) Added `showLegend` property to Speck viewer, which allows users to show a color legend for atoms shown on the canvas.
* [#641](https://github.com/plotly/dash-bio/pull/641) Added `style` property to Speck and Molecule3dViewer to enable generic style overrides on the plot div.

### Changed
* [#589](https://github.com/plotly/dash-bio/pull/589) Removed hardcoded clustergram linkage method, added parameter `link_method` instead.
* [#592](https://github.com/plotly/dash-bio/pull/592) Changed default plot colors of Clustergram to color vision deficiency friendly colormap (for more info see [#450](https://github.com/plotly/dash-bio/issues/450)).


## [0.8.0] - 2021-09-27

### Fixed
* [#576](https://github.com/plotly/dash-bio/pull/576) Fixed abnormal memory consumption with Molecule3dViewer component when selecting residues or rotating the molecule (for more info see [#511](https://github.com/plotly/dash-bio/issues/511)).
* [#575](https://github.com/plotly/dash-bio/pull/575) Bumped Ideogram version to 1.6.0 to fix erratic annotations behavior (for more info see [#524](https://github.com/plotly/dash-bio/issues/524)).

### Added
* [#567](https://github.com/plotly/dash-bio/pull/567) Added VariantMap component (see [#504](https://github.com/plotly/dash-bio/pull/504) for original PR).
* [#573](https://github.com/plotly/dash-bio/pull/573) Added the ability to configure the FornaContainer hover info with `hoverPattern` prop and interpolated node keys (for more info see [#519](https://github.com/plotly/dash-bio/issues/519)).
* [#579](https://github.com/plotly/dash-bio/pull/579) Added ability to resize the NeedlePlot component (for more info see [#545](https://github.com/plotly/dash-bio/issues/545)).
* [#583](https://github.com/plotly/dash-bio/pull/583) Added the ability to manually set Sequence ID's for AlignmentChart component (for more info see [#421](https://github.com/plotly/dash-bio/issues/421)).

## [0.7.1] - 2021-07-26

### Fixed
* [#562](https://github.com/plotly/dash-bio/pull/562) Repeated re-rendering of the Molecule3dViewer component caused the viewer zoom to decrease multiplicatively.
This fix also exposes the `zoom` and `zoomTo` props for this component.
* [#565](https://github.com/plotly/dash-bio/pull/565) Fixed major domain annotation positioning for the NeedlePlot component and exposed `textangle` prop to allow domain annotation text to be angled relative to the horizontal axis.

### Changed
- [#563](https://github.com/plotly/dash-bio/pull/563) Changed package scripts to 3 main build scripts: `build:js`, `build:backends`, and `build` to combined them. This brings the dash-bio build process in-line with the process for other Dash component libraries. As part of this change, `__init__.py` now also uses relative imports to load components (for more info, see [#534](https://github.com/plotly/dash-bio/issues/534)).

### Added
* [#564](https://github.com/plotly/dash-bio/pull/564) Added component generation support for Dash Julia.
* [#565](https://github.com/plotly/dash-bio/pull/565) Added `margins` and `clickData` props to NeedlePlot to expose event data for callbacks.

## [0.7.0] - 2021-04-19

### Fixed
* [#547](https://github.com/plotly/dash-bio/pull/547) `sideByside` prop fix for NglMoleculeViewer  component when `ALL` chains are visualized.

### Added
* [#543](https://github.com/plotly/dash-bio/pull/543) Added Dash Pileup component.
* [#547](https://github.com/plotly/dash-bio/pull/547) Added shapes and isosurfaces props to 3dMoleculeViewer to enable rendering additional features on the molecule.
* [#553](https://github.com/plotly/dash-bio/pull/553) Added source mapping.
* [#554](https://github.com/plotly/dash-bio/pull/554) Added additional props and arbitrary layout arguments to VolcanoPlot.

### Changed
- [#550](https://github.com/plotly/dash-bio/pull/548) Updated CONTRIBUTING.md andbasic demo app structure. In addition, removed residual code and pre-deploy scripts associated with now-discontinued Dash Bio gallery.

## [0.6.1] - 2021-02-15
### Fixed
* [#544](https://github.com/plotly/dash-bio/pull/544) Miscellaneous fixes for NglMoleculeViewer component.

## [0.6.0] - 2021-01-28
### Added
* [#537](https://github.com/plotly/dash-bio/pull/537) Added Dash-IGV component.

## [0.5.1] - 2020-12-27
### Fixed
* [#536](https://github.com/plotly/dash-bio/pull/536) Fixed abandoned resource vulnerability with CircosJS fork.

## [0.5.0] - 2020-10-05
### Added
* [#496](https://github.com/plotly/dash-bio/pull/496) Added Dash-NGL-Moleculeviewer component.

### Fixed
* [#512](https://github.com/plotly/dash-bio/pull/512) Fixed bug involving clustergrams not being visible in dendograms.

## [0.4.8] - 2020-03-16
### Changed
* [#489](https://github.com/plotly/dash-bio/pull/489) Renamed async modules with hyphen `-` instead of tilde `~`
* [#494](https://github.com/plotly/dash-bio/pull/494) Update from React 16.8.6 to 16.13.0

### Added
* [#492](https://github.com/plotly/dash-bio/pull/492) Added working support of
  labels in Clustergram.

## [0.4.7] - 2020-02-21
### Added
* [#478](https://github.com/plotly/dash-bio/pull/478) Added support of
  DataFrame as Clustergram input.

## [0.4.6] - 2020-01-07
### Fixed
* [#458](https://github.com/plotly/dash-bio/pull/458) Fixed reordering bug of
  row and column indices following clustering in Clustergram component.

## [0.4.5] - 2019-11-26
* [#452](https://github.com/plotly/dash-bio/pull/452) Fix issue finding CDN resources when using `serve_locally=False`

## [0.4.4] - 2019-11-21
### Fixed
* [#423](https://github.com/plotly/dash-bio/pull/423) Fixed internal method
  call in Clustergram component.

## [0.4.3] - 2019-11-18
### Changed
* [#438](https://github.com/plotly/dash-bio/pull/438/) Updated FornaContainer dependency to a version without extraneous `console.log` calls.

## [0.4.2] - 2019-11-15
### Fixed
* [#437](https://github.com/plotly/dash-bio/pull/437) Fix IE11 compatibility issues and ES5 compatibility and validation

## [0.4.1] - 2019-11-08
### Fixed
* [#434](https://github.com/plotly/dash-bio/pull/434) Fixed FornaContainer selector issue, in which FornaContainer styles were being applied to all svg elements on the page.

## [0.4.0] - 2019-11-05
### Added
* [#430](https://github.com/plotly/dash-bio/pull/430) Async AlignmentChart, Circos, Ideogram, Molecule2dViewer, Molecule3dViewer, NeedlePlot, OncoPrint, SequenceViewwer and Speck components

## [0.3.0] - 2019-10-22

### Added

* Added FornaContainer component for RNA secondary structure analysis.

## [0.2.0] - 2019-10-18

### Fixed

* Fixed AlignmentChart error in which `colorscale` being undefined
  caused rendering to fail.
* Fixed AlignmentChart PropType for `eventDatum` to `string` (which is
  what gets returned).
* Fixed Circos error in which `tracks` variable being undefined caused
  rendering to fail.
* Fixed Clustergram error in which `display_ratio` (a float or a list)
  was used as a list instead of `self._display_ratio`, which always
  has the type `list`.
* Fixed Molecule2dViewer error in which `modelData` being undefined
  caused rendering to fail.
* Fixed Molecule2dViewer PropType for `source` and `target` atoms
  within the `links` property to also include `PropTypes.shape`.
* Fixed Molecule3dViewer error in which there was no re-rendering upon
  a change in the `selectionType` prop.
* Fixed SequenceViewer error in which the component initially rendered
  with coverage that had no defined `onClick` behavior.

### Added

* Added re-rendering for Molecule2dViewer and Molecule3dViewer upon
  the `selectedAtomIds` prop being updated. (This lets the user write
  to the `selectedAtomIds` prop through a Dash component.)
* Added re-rendering for SequenceViewer upon the `coverageClicked`
  prop being updated.

### Removed

* Removed AlignmentViewer component
  ([#414](https://github.com/plotly/dash-bio/issues/414))

## [0.1.4] - 2019-08-02

### Changed
* Updated core dependency to `dash>=1.0.0`.

## [0.1.3] - 2019-07-31

### Changed
* Renamed Clustergram parameters `hide_labels` and `symmetric_value` into
  `hidden_labels` and `center_values` respectively.

### Fixed
* Fixed issue with Molecule2dViewer not displaying triple bonds.

## [0.1.2] - 2019-07-13

### Changed
* Made Speck component compatible with refactored Speck library.
* Optimized Speck component further to increase performance.

### Added
* Added default props to Molecule3dViewer component.
* Added zoom/pan and export SVG capabilities to Circos.

## [0.1.1] - 2019-06-06

### Added
* Added Molecule2dViewer component.

### Changed
* Refactored Speck component and implemented general bug fixes.

### Fixed
* Fixed issue with Speck not responding to preset changes.

## [0.1.0] - 2019-05-27

### Removed
* Removed all parsing tools in `dash_bio.utils` to a separate package,
  `dash_bio_utils`.

## [0.0.11] - 2019-05-09

### Added
* Added to xyz_reader the ability to handle whitespace at the
  beginning and end of a line (in data file).
* Added a working link to the JS distribution, so serving scripts
  locally is no longer necessary.

## [0.0.10] - 2019-04-30

### Fixed
* Fixed homepage link in package metadata.

## [0.0.9] - 2019-04-29

### Fixed
* Fixed issue with Clustergram rows and columns reordering incorrectly
  on the heatmap when precomputed traces are used to generate the
  figure.
* Fixed issue with Speck not rendering unless it is attached to a
  callback.
* Prevented Speck from trying to calculate a system with no atom.
* Let Clustergram render even when row and column labels are not
  specified, by adding default values.
* Allowed multiple SequenceViewer components to render on the same
  application.

### Changed
* Changed Clustergram to only return a figure by default, so that
  values no longer need to be unpacked.
* Changed Molecule3dViewer's `selectionType` prop to accept all-
  lowercase values.

### Added
* Added to Clustergram the ability to generate a "curve dictionary" to
  translate curve number (available in hoverData/clickData) to the row
  or column cluster it represents on the graph.

## [0.0.8] - 2019-01-04

### Fixed
* Fixed issue with Clustergram not reordering rows and columns after
  clustering.

### Removed
* Removed mentions of Dash events in OncoPrint component.
* Removed properties which weren't used in Ideogram component.

### Changed
* Changed property `fullChromosomeLabels` so that it can be updated
  using dash callbacks.
* Changed Imputer (deprecated) to SimpleImputer in Clustergram
  component.
* Changed property name `impute_function` to `imputer_parameters` in
  Clustergram component.
* Changed install requirement to Dash version 0.40.0 or greater.

### Added
* Added ability to define custom colors in style parser for
  Molecule3D.

## [0.0.7] - 2019-26-02

### Changed
* Changed unicode right arrow to greater-than sign in Circos for
  compatibility with Python 2.7.

## [0.0.6] - 2019-22-02

### Added
* Added requirements from files in `utils`, as well as from
  pure-Python components, to setup install requirements.
* Added more descriptive prop descriptions for Dash Ideogram.

## [0.0.5] - 2019-15-02

### Changed
* Changed filenames in `dash_bio/utils/` folder to be snake case
  instead of camel case.

## [0.0.4] - 2019-11-02

### Added
* Added recent update to Speck library to fix jumpy behavior on
  click-and-drag.

## [0.0.3] - 2019-06-02

### Added
* Added variables to define strings used in `_volcano.py` graph
  labels.

## [0.0.2] - 2019-05-02

### Fixed
* Fixed incompatibility issues with Dash `0.36.0`.

### Removed
* Removed all mentions of `fireEvent` and anything else that used Dash
  events (which have been removed).

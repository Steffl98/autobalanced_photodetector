# Auxiliary PSU Import

- `Power_Interfaces` contains the `Auxiliary_PSU` child sheet: +/-12 V and +/-5 V.
- Main PCB contains its 73 footprints, 255 track/via items and 18 zones.
- Imported references are offset by 100: U1 -> U101, C1 -> C101, etc.
- Input return is `PGND`; isolated output return is `AGND`. They are not shorted.
- Rails: `VCC_12V`, `VEE_12V`, `VCC_5V`, `VEE_5V`.
- `VIN_12V` and `VFLY_12V` are aliases of the shared primary-side 12-V input.
- Datasheets use project-relative paths. Existing source PSU files are unchanged.
- Corrected imported U106: source incorrectly assigned a 1206 resistor footprint;
  now uses the same exposed-pad TSSOP-16 footprint as U101, at its existing position.
- Other 111 schematic components are not placed on the PCB yet. Board outline and
  inherited schematic/ERC issues remain; this is not a fabrication release.
- Import check: no unrouted PSU nets, copper clearance violations, silkscreen
  collisions or imported schematic/PCB net conflicts. Two ERC naming warnings
  reflect VIN_12V/VFLY_12V and GND_IN/PGND interface aliases.
- Standalone Eaton vendor libraries/3D files remain local and Git-ignored because
  of their redistribution restrictions. Symbols/footprints are embedded in design
  files; optional vendor 3D rendering requires the local package.

Import checks and original backups are outside this repository:
`../../../local_only/pcb_backups/2026-11-10_repo_psu_import/`

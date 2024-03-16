# DNOTQ KiCAD Library

Parts and footprints used in DNOTQ designs.

To set up the library:

- Clone the repository to whereever you want on your system.
- Start KiCAD, select `Preferences -> Configure Paths`
- Create a new Environment Variable called `DNOTQLIB` and set the path to where you cloned the repository:

![Environment Variable Setup](kicad_env_vars.png "Environment Variable Setup")

- Select `Preferences -> Manage Symbol Libraries...`
- Click the `+` icon "Add empty row to table", then:
   * Check the `Active` checkbox
   * For the "Nickname" enter `dnotq_library`
   * For the "Library Path" enter `${DNOTQLIB}/library/dnotq_kicad_library.kicad_sym`
   * For the "Library Format" select `KiCad`
   * For the "Description" enter `DNOTQ Symbols`

![Manage Symbol Libraries](kicad_sym_libs.png "Manage Symbol Libraries")

Setting up the footprints is the same process as the symbols:

- Select `Preferences -> Manage Footprint Libraries...`
- Click the `+` icon "Add empty row to table", then:
   * Check the `Active` checkbox
   * For the "Nickname" enter `dnotq_footprint`
   * For the "Library Path" enter `${DNOTQLIB}/dnotq.pretty`
   * For the "Library Format" select `KiCad`
   * For the "Description" enter `DNOTQ Footprints`

![Manage Footprint Libraries](kicad_foot_libs.png "Manage Footprint Libraries")

All models for footprints use the `${DNOTQLIB}` environment variable prefix, so all previews of boards using these parts should "just work" as expected.

![Footprint Properties 3D Model](kicad_model_setup.png "Footprint Properties 3D Model")

Symbols and footprints from the libarary will use the `dnotq_library` and `dnotq_footprint` nicknames set in the steps above.  This allows the entire library to be located or moved anywhere by simply changing the one `${DNOTQLIB}` environment variable.

![Symbol and footprint use library nicknames](kicad_using_sym_foot.png "Symbol and footprint use library nicknames")

Before submitting a mount, make sure it follows the following mount submission rules:

### Before you submit, consider the rules

Each mount must adhere to the following rules to be eligible for inclusion in Mounts:

- Submitted mounts must be compatible with ERCF v2 or v3.
- Mounts must be original work by the author. When submitting the mount to this repository, the author confirms that they have not stolen this mount from another user or another website
- Mounts in this repository are goverened by the repository license: [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html). If you do not agree with this license, please don't submit your mount here.
- Mounts must be tested, at least by the author. Ideally, more users have built and tested your mount. Join the [ERCF Discord](https://discord.com/channels/1267663557999329371/1310278996503826585) to find testers! Please don't submit untested mounts.
- Mounts must not represent slight mountifications of existing mounts/existing ERCF parts. (e.g. inconsequential addition of chamfers/fillets or other changes that don't affect the functionality of a part in a meaningful way)
- Avoid mandatory use of glue or similar assembly methods. Try to stick to the existing fastener hardware and assembly methods of ERCF and VoronDesign printers
- Mounts must aim for the same standard that ERCF uses and VoronDesign applies to their printers. As such:
  - Mount files must be provided as STL/OBJ and in at least one CAD format (e.g. STEP, IGES, F3D, etc., **open formats like STEP are preferred**)
  - When submitting STLs, please try to submit them in binary format as this saves space, and allows to preview the STL files on GitHub
  - Printable mount files must be oriented in their intended printing orientation. You can use, e.g. PrusaSlicer to rotate your STLs correctly
  - Printable mount files must be printable without support. If supports are absolutely needed, they should be baked into the mountel as break-away supports.
  - Printable mount files must be free of errors (i.e. when importing into a Slicer, no errors should be reported)
  - Submitted mount files must not include unmountified ERCF parts
  - Submitted documents contain no sensitive data (e.g. API keys)

### Anatomy of a mount: folder structure, filenames

If you want to submit a mount and require a starting point, check out the [sample mount folder zip file](https://github.com/VoronDesign/VoronUsers/raw/main/sample_mount.zip). Simply unzip the contents over your local repository (make sure the `SAMPLE_AUTHOR` folder ends up in the `printer_mounts` folder) and change folder names and contents accordingly.

In order to help users to find the appropriate files of your mount, please consider the following instructions when submitting your mount:

- To submit your mount, put it in the `Mounts/` folder
- Create a subfolder with your name in the appropriate folder, then create further subfolders for each of your mounts
- The following folder tree shows the preferred file layout of your mount. While deviations from this format can be discussed on a case-by-case basis, it is strongly encouraged to adhere to this structure to speed up the review process:
```
.
└── printer_mounts/
    └── FHeilmann/
        ├── my_mount/
        │   ├── STL/
        │   │   ├── [a]_accent_part.stl
        │   │   └── non_accent_part.stl
        │   ├── CAD/
        │   │   ├── step_file.step
        │   │   └── fusion.f3d
        │   ├── Images/
        │   │   ├── printed.jpg
        │   │   └── assembly_instructions.png
        │   ├── OTHER/
        │   │   ├── BOM.xlsx
        │   │   └── assembly_instructions.pdf
        │   ├── README.md
        │   └── .metadata.yml
        └── another_mount/
            ├── STL/
            │   └── part_1.stl
            ├── CAD/
            ├── Images/
            ├── OTHER/
            ├── README.md
            └── .metadata.yml
```
- **All filenames and foldernames in Mounts must not have spaces in them!  Please stick to letters `a-zA-Z`, numbers `0-9`, underscores `_`, hyphens `-`, brackets `[]()` and periods `.`**
- Please keep in mind that for file and folder names, capitalization matters!  Your links and `.metadata.yml` must use the same capitalization your folders and files do.
- You can optionally indicate the color and quantity of printable parts:
  - Accent color: [a]_part_xyz.stl
  - Opaque color (Blocks light): [o]_part_xyz.stl
  - Clear/transparent color (Allows light): [c]_part_xyz.stl
  - Quantity, if more than one is needed: part_xyz_x4.stl 
- Please add a short README.md to each mount folder to provide the user with additional information, e.g. 
  - Images you provided with your mount
  - BOM for your mount (if required)
  - Assembly instructions
  - Vendor links for specific parts

Thank you for taking the time to read these rules. Head over to the [submission tutorial](How-to-Submit-to-Mounts) to learn how you can add your mount to this repository and submit it for review.
# citygml2-to-citygml3

A small Java program used to transform CityGML v2.0 to CityGML v3.0 files.

This project is still in early developement und subject to changes.

### How to run
The program can be executed by running the `Run.bat` file (in Windows).

The result is by default saved in [CityGML_v3_Transformed.gml](CityGML_v3_Transformed.gml) (only visible after the program is complete).

### Command line
Alternatively, the program can also be executed using the command line:
```batch
java -jar Transform.jar SourceXMLFile XSLFile OutputXMLFile
```
where 

| Arguments        | Description           | Default  |
| ------------- |:-------------| -----|
| `SourceXMLFile`      | The location of the source CityGML v2.0 file | `input/CityGML_v2.gml` |
| `XSLFile`      | The location of the XSL file used for transformation | `Transform.xsl` |
| `OutputXMLFile`      | The location of the transformed CityGML v3.0 file | `output/CityGML_v3_Transformed.gml` |

For reference, the [CityGML_v3.gml](output/CityGML_v3.gml) can be used as an example of how the transformed file should look like.

### Notes
Currently, only the `Building` module is supported.

The implementation was tested on a limited number of samples provide in CityGML 3.0 and thus that may not solve all use cases.

Also note that the XML schemata for CityGML 3.0 are still in active development and might change in the near future. For the latest XSD files, please refer to the [OGC CityGML 3.0 Encodings GitHub page](https://github.com/opengeospatial/CityGML-3.0Encodings).
# Change Log/Revision History

= 1.1.5 =
=========
- Conversion to Maven build and Maven dependencies.

= 1.1.4 =
=========
- lenient date parsing to handle both yyyyMMddHHmmss and yyyyMMddHHmmssZ time standards in the MSH

= 1.1.3 =
=========
- Expansion of PV1.2 patient class value set to include:

```
  ----------------------------------
  | Value   |   Description        |
  |---------+----------------------|
  |   E     |   Emergency          |
  |   I     |   Inpatient          |
  |   O     |   Outpatient         |
  |   P     |   Preadmit           |
  |   R     |   Recurring patient  |
  |   B     |   Obstetrics         |
  |   C     |   Commercial Account |
  |   N     |   Not Applicable     |
  |   U     |   Unknown            |
  ----------------------------------
```

= 1.1.2 =
=========
- For all segments, the restriction on maximum field count has been set to
  unbounded. Segments may now contain fields in addition to the minimum required
  fields, documented in the position paper. These additional fields will be
  ignored by the MDM unwrap functionality.

= 1.1.1 =
=========
- PID.11 XAD country code data type restriction modified to allow string
  to be supplied.

= 1.1.0 =
=========
- Added functionality for extracting an MDM message's field contents.
- Added support for 'identifier type code' in XCN data type (used in PV1.9).
- Modified country codes from 'AU' to 'AUS' (ISO 3166).
- Consolidated various segment field values into HL7 data type classes.
- Javadoc modifications to reflect changes to library as well as clarifying
  usage and expected values.
- Removed core functionality from the MDMUtil class. Generation/extraction
  of messages is handled by relevant each member types class methods (see sample
  code and Javadoc for more detailed usage instructions):
  1.  generateMDMMessage() --> class 'toString()' method produces formatted
      string. Messages, segments, fields and value types make use of this.
  2. extractMDMMessage() --> class 'parse()' method extracts and populates
      object. Messages, segments, fields and value types make use of this.

= 1.0.0 =
=========
Initial Version
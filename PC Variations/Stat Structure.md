## Terminology:

- A "Stat" is a "StatKind" mapped to a "StatValue".
- "StatValues" is a struct of two float Variables: a "Current" and a "Max".
- A "StatValueID" is a struct of two Enum values: a "StatKind" and a "StatValueType" eg.: "Current", "Health".
    - "Health" and "Energy" are "StatKinds".
    - "Current" is a singular "StatValue" as well as a "StatValueType".

* * *

## What you can Get:

- MapOfStats
- StatValuesFromKind
- StatValueFromID

* * *

## What you can Set:

- StatValueByID (Set to, or Change by, an input Float)
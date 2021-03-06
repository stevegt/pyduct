# pyduct
HVAC duct pressure drop, flowrate calculations, and sizing. Uses equal friction method.

Created for college computer methods course using Python 3.5.2. YMMV.

![version](https://img.shields.io/badge/version-1.0-brightgreen.svg)
![Python 3.4+](https://img.shields.io/badge/Python-3.4%2B-blue.svg)

### Example Input file

```
# Lines starting with a # character are comments to be ignored
# You may have comment lines anywhere in the file
#
# Other lines in the file are identified by specific KEYWORDS, followed by data
# KEYWORDS may include Capital letters, but capitalization will be ignored
# blank lines are also allowed and should be ignored

# each line stands alone, and there is no required ORDER to the file

title, 'A Fictitious Small Office Building'
#             in. wg
fan_pressure, 1.000
#            lbm/cubic foot
air_density, 0.075
#          feet
roughness, 0.0003
#         up, nearest, none
rounding, none

# duct fitting entries are a Id number, followed by a fitting type,
# followed by data

#          ID     Fitting Type    Fan-side-ID     Flow or Length (CFM or feet)
fitting,   1,  Air_Handling_Unit
fitting,   3,  Duct                 , 1             , 50
fitting,   4,  Tee                  , 3
fitting,   5,  Duct                 , 4-main        , 20
fitting,   6,  Tee                  , 5
fitting,   7,  Duct                 , 6-main        , 80
fitting,   8,  Tee                  , 7
fitting,   9,  Elbow                , 8-main
fitting,  10,  Duct                 , 9             , 75
fitting,  11,  Diffuser             , 10            , 125
fitting,  12,  Duct                 , 8-branch      , 25
fitting,  13,  Diffuser             , 12            , 130
fitting,  14,  Duct                 , 6-branch      , 80
fitting,  16,  Diffuser             , 14            , 135
fitting,  17,  Duct                 , 4-branch      , 55
fitting,  18,  Tee                  , 17
fitting,  19,  Duct                 , 18-main       , 60
fitting,  20,  Diffuser             , 19            , 150
fitting,  21,  Duct                 , 18-branch     , 40
fitting,  22,  Elbow                , 21
fitting,  23,  Duct                 , 22            , 45
fitting,  24,  Diffuser             , 23            , 105
```

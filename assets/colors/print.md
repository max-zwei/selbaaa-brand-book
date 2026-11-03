# Print color palette

CMYK colors the selba palette, paired with the original sRGB HEX references. Token names and palette membership match the [digital palette](digital.md#colors).

## Colors

The selba palette contains a shared Primary color, three groups for Morning, Day, and Night products, and the neutrals Ink and Screen. Each group has a main color and three secondary colors. The descriptive suffixes identify those existing secondary colors; they do not assign new product or interaction meanings.

### Palette reference

| Token | Palette role | sRGB | C (%) | M (%) | Y (%) | K (%) |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `primary` | Primary | `#EB341B` | 0 | 78 | 89 | 8 |
| `morning` | Morning — main | `#499ACD` | 64 | 25 | 0 | 20 |
| `morning-pink` | Morning — secondary pink | `#F77EAD` | 0 | 49 | 30 | 3 |
| `morning-sun` | Morning — secondary yellow | `#F5D91B` | 0 | 11 | 89 | 4 |
| `morning-lime` | Morning — secondary lime | `#BBE132` | 17 | 0 | 78 | 12 |
| `day` | Day — main | `#FF7852` | 0 | 53 | 68 | 0 |
| `day-blue` | Day — secondary blue | `#18498F` | 83 | 49 | 0 | 44 |
| `day-torquoise` | Day — secondary torquoise | `#00CC99` | 100 | 0 | 25 | 20 |
| `day-purple` | Day — secondary purple | `#AC5BAC` | 0 | 47 | 0 | 33 |
| `night` | Night — main | `#0B1946` | 84 | 64 | 0 | 73 |
| `night-lavender` | Night — secondary lavender | `#B0AEC9` | 12 | 13 | 0 | 21 |
| `night-sage` | Night — secondary sage | `#BDDC9F` | 14 | 0 | 28 | 14 |
| `night-sand` | Night — secondary sand | `#D7C9C2` | 0 | 7 | 10 | 16 |
| `ink` | Ink — dark neutral | `#1E1E1E` | 0 | 0 | 0 | 88 |
| `screen` | Screen — paper white | `#FFFFFF` | 0 | 0 | 0 | 0 |

### Design tokens

```yaml
colors:
  primary: [0, 78, 89, 8]
  morning: [64, 25, 0, 20]
  morning-pink: [0, 49, 30, 3]
  morning-yellow: [0, 11, 89, 4]
  morning-lime: [17, 0, 78, 12]
  day: [0, 53, 68, 0]
  day-blue: [83, 49, 0, 44]
  day-torquoise: [100, 0, 25, 20]
  day-purple: [0, 47, 0, 33]
  night: [84, 64, 0, 73]
  night-lavender: [12, 13, 0, 21]
  night-sage: [14, 0, 28, 14]
  night-sand: [0, 7, 10, 16]
  ink: [0, 0, 0, 88]
  screen: [0, 0, 0, 0]
```

### Application

Use the documented groups and retain their token names when assigning roles in a design. Palette membership alone does not establish a readable text/background combination; check contrast in the actual application. Morning, Day, and Night are palette groups, not automatic light/dark themes or status colors.
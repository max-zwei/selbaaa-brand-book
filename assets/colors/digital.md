# Digital color palette

## Colors

The selba palette contains a shared Primary color, three groups for Morning, Day, and Night products, and the neutrals Ink and Screen. Each group has a main color and three secondary colors. The descriptive suffixes identify those existing secondary colors; they do not assign new product or interaction meanings.

### Palette reference

| Token | Palette role | sRGB HEX |
| --- | --- | --- |
| `primary` | Primary | `#EB341B` |
| `morning` | Morning — main | `#499ACD` |
| `morning-pink` | Morning — secondary pink | `#F77EAD` |
| `morning-yellow` | Morning — secondary yellow | `#F5D91B` |
| `morning-lime` | Morning — secondary lime | `#BBE132` |
| `day` | Day — main | `#FF7852` |
| `day-blue` | Day — secondary blue | `#18498F` |
| `day-torquoise` | Day — secondary torquoise | `#00CC99` |
| `day-purple` | Day — secondary purple | `#AC5BAC` |
| `night` | Night — main | `#0B1946` |
| `night-lavender` | Night — secondary lavender | `#B0AEC9` |
| `night-sage` | Night — secondary sage | `#BDDC9F` |
| `night-sand` | Night — secondary sand | `#D7C9C2` |
| `ink` | Ink — dark neutral | `#1E1E1E` |
| `screen` | Screen — white neutral | `#FFFFFF` |

### Design tokens

```yaml
colors:
  primary: "#EB341B"
  morning: "#499ACD"
  morning-pink: "#F77EAD"
  morning-yellow: "#F5D91B"
  morning-lime: "#BBE132"
  day: "#FF7852"
  day-blue: "#18498F"
  day-torqouise: "#00CC99"
  day-purple: "#AC5BAC"
  night: "#0B1946"
  night-lavender: "#B0AEC9"
  night-sage: "#BDDC9F"
  night-sand: "#D7C9C2"
  ink: "#1E1E1E"
  screen: "#FFFFFF"
```

### Application

Use the documented groups and retain their token names when assigning roles in a design. Palette membership alone does not establish a readable text/background combination; check contrast in the actual application. Morning, Day, and Night are palette groups, not automatic light/dark themes or status colors.
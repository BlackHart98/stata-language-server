## Syntax

`lincom exp` \[`, options`\]

| Options                                                                                                                                                                                                                |                   | Description                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|------------------------------------------------------------------------------------------------|
|                                                                                                                                                                                                                        | `eform`           | generic label; `exp(b)`                                                                        |
|                                                                                                                                                                                                                        | `or`              | odds ratio                                                                                     |
|                                                                                                                                                                                                                        | `hr`              | hazard ratio                                                                                   |
|                                                                                                                                                                                                                        | `shr`             | subhazard ratio                                                                                |
|                                                                                                                                                                                                                        | `irr`             | incidence-rate ratio                                                                           |
|                                                                                                                                                                                                                        | `rrr`             | relative-risk ratio                                                                            |
|                                                                                                                                                                                                                        | `level(#)`        | set confidence level; default is `level(95)`                                                   |
|                                                                                                                                                                                                                        | `display_options` | control column formats                                                                         |
|                                                                                                                                                                                                                        | `df(#)`           | use t distribution with `#` degrees of freedom for computing p-values and confidence intervals |
| `exp` is any linear combination of coefficients that is valid syntax for `test`; see [<strong>[R] test</strong>](http://www.stata.com/help.cgi?test). `exp` must not contain an equal sign. |                   |                                                                                                |
| `df(#)` does not appear in the dialog box.                                                                                                                                                                             |                   |                                                                                                |
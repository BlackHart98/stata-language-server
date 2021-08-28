## Syntax

`zip`
[depvar](http://www.stata.com/help.cgi?depvar)
\[[indepvars](http://www.stata.com/help.cgi?indepvars)\]
_\[`if`\] \[`in`\]_ \[`weight`\]`,`  
`inflate(`[varlist](http://www.stata.com/help.cgi?varlist)\[`,`
`offset(varname)`\]\|`_cons)` \[`options`\]

| options                                                                                                                                                                                                                                                                                                                      |                                | Description                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Model                                                                                                                                                                                                                                                                                                                        |                                |                                                                                                                                                  |
| \*                                                                                                                                                                                                                                                                                                                           | `inflate()`                    | equation that determines whether the count is zero                                                                                               |
|                                                                                                                                                                                                                                                                                                                              | `noconstant`                   | suppress constant term                                                                                                                           |
|                                                                                                                                                                                                                                                                                                                              | `exposure(varname_e)`          | include `ln(varname_e)` in model with coefficient constrained to 1                                                                               |
|                                                                                                                                                                                                                                                                                                                              | `offset(varname_o)`            | include `varname_o` in model with coefficient constrained to 1                                                                                   |
|                                                                                                                                                                                                                                                                                                                              | `constraints(constraints)` | apply specified linear constraints                                                                                                               |
|                                                                                                                                                                                                                                                                                                                              | `collinear`                    | keep collinear variables                                                                                                                         |
|                                                                                                                                                                                                                                                                                                                              | `probit`                       | use probit model to characterize excess zeros; default is logit                                                                                  |
| SE/Robust                                                                                                                                                                                                                                                                                                                    |                                |                                                                                                                                                  |
|                                                                                                                                                                                                                                                                                                                              | `vce(vcetype)`                 | `vcetype` may be `oim`, `robust`, `cluster clustvar`, `opg`, `bootstrap`, or `jackknife`                                                       |
| Reporting                                                                                                                                                                                                                                                                                                                    |                                |                                                                                                                                                  |
|                                                                                                                                                                                                                                                                                                                              | `level(#)`                     | set confidence level; default is `level(95)`                                                                                                     |
|                                                                                                                                                                                                                                                                                                                              | `irr`                          | report incidence-rate ratios                                                                                                                     |
|                                                                                                                                                                                                                                                                                                                              | `nocnsreport`                  | do not display constraints                                                                                                                       |
|                                                                                                                                                                                                                                                                                                                              | `display_options`              | control columns and column formats, row spacing, line width, display of omitted variables and base and empty cells, and factor-variable labeling |
| Maximization                                                                                                                                                                                                                                                                                                                 |                                |                                                                                                                                                  |
|                                                                                                                                                                                                                                                                                                                              | `maximize_options`             | control the maximization process; seldom used                                                                                                    |
|                                                                                                                                                                                                                                                                                                                              | `coeflegend`                   | display legend instead of statistics                                                                                                             |
| \* `inflate(varlist`\[`, offset(varname)`\]\|`_cons)` is required.                                                                                                                                                                                                                                                     |                                |                                                                                                                                                  |
| `indepvars` and `varlist` may contain factor variables; see [<strong>fvvarlist</strong>](http://www.stata.com/help.cgi?fvvarlist).                                                                                                                                                                |                                |                                                                                                                                                  |
| `bayes`, `bootstrap`, `by`, `fp`, `jackknife`, `rolling`, `statsby`, and `svy` are allowed; see [<strong>prefix</strong>](http://www.stata.com/help.cgi?prefix). For more details, see [<strong>[BAYES]</strong> bayes: zip](http://www.stata.com/help.cgi?bayes_zip). |                                |                                                                                                                                                  |
| Weights are not allowed with the [<strong>bootstrap</strong>](http://www.stata.com/help.cgi?bootstrap) prefix.                                                                                                                                                                                    |                                |                                                                                                                                                  |
| `vce()` and weights are not allowed with the [<strong>svy</strong>](http://www.stata.com/help.cgi?svy) prefix.                                                                                                                                                                                    |                                |                                                                                                                                                  |
| `fweight`s, `iweight`s, and `pweight`s are allowed; see [<strong>weight</strong>](http://www.stata.com/help.cgi?weight).                                                                                                                                                                          |                                |                                                                                                                                                  |
| `coeflegend` does not appear in the dialog box.                                                                                                                                                                                                                                                                              |                                |                                                                                                                                                  |
| See [<strong>[R]</strong> zip postestimation](http://www.stata.com/help.cgi?zip_postestimation) for features available after estimation.                                                                                                                                                          |                                |                                                                                                                                                  |
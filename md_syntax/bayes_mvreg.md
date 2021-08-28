## Syntax

`bayes` \[`, bayesopts`\] `: mvreg depvars =`
[indepvars](http://www.stata.com/help.cgi?indepvars)
_\[`if`\] \[`in`\]_ \[`weight`\] \[`,`
`options`\]

| Options                                                                                                                                                                                                                                         |                   | Description                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------------------------------------------------------|
| Model                                                                                                                                                                                                                                           |                   |                                                       |
|                                                                                                                                                                                                                                                 | `noconstant`      | suppress constant term                                |
| Reporting                                                                                                                                                                                                                                       |                   |                                                       |
|                                                                                                                                                                                                                                                 | `display_options` | control spacing, line width, and base and empty cells |
|                                                                                                                                                                                                                                                 | `level(#)`        | set credible level; default is `level(95)`            |
| `indepvars` may contain factor variables; see [<strong>fvvarlist</strong>](http://www.stata.com/help.cgi?fvvarlist).                                                                                                 |                   |                                                       |
| `fweight`s are allowed; see [<strong>weight</strong>](http://www.stata.com/help.cgi?weight).                                                                                                                         |                   |                                                       |
| `bayes: mvreg, level()` is equivalent to `bayes, clevel(): mvreg`.                                                                                                                                                                      |                   |                                                       |
| For a detailed description of `options`, see [<var class="command">Options</var><strong></strong>](mvreg##options) in [<strong>[MV]</strong> mvreg](http://www.stata.com/help.cgi?mvreg). |                   |                                                       |

bayesopts

Description

[<strong>Priors</strong>](bayes##priors_options)

\*

`gibbs`

specify Gibbs sampling; available only with normal priors for regression
coefficients and multivariate Jeffreys prior for covariance

\*

`normalprior(#)`

specify standard deviation of default normal priors for regression
coefficients; default is `normalprior(100)`

INCLUDE help bayesmh\_prioropts

[<strong>Simulation</strong>](bayes##simulation_options)

INCLUDE help bayesmh\_simopts

[<strong>Blocking</strong>](bayes##blocking_options)

\*

`blocksize(#)`

maximum block size; default is `blocksize(50)`

INCLUDE help bayesmh\_blockopts

|     |              |                                    |
|-----|--------------|------------------------------------|
| \*  | `noblocking` | do not block parameters by default |

[<strong>Initialization</strong>](bayes##initialization_options)

INCLUDE help bayesmh\_initopts

|     |           |                                                                  |
|-----|-----------|------------------------------------------------------------------|
| \*  | `noisily` | display output from the estimation command during initialization |

[<strong>Adaptation</strong>](bayes##adaptation_options)

INCLUDE help bayesmh\_adaptopts

[<strong>Reporting</strong>](bayes##reporting_options)

INCLUDE help bayesecmd\_reportopts

[<strong>Advanced</strong>](bayes##advanced_options)

INCLUDE help bayesmh\_advancedopts

|                                                                                                                                                                                                                                                                                                                                      |     |     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|-----|
| \* Starred options are specific to the `bayes` prefix; other options are common between `bayes` and [<strong>bayesmh</strong>](http://www.stata.com/help.cgi?bayesmh).                                                                                                                                    |     |     |
| Options `prior()` and `block()` can be repeated.                                                                                                                                                                                                                                                                                     |     |     |
| [<var class="command">priorspec</var><strong></strong>](bayesmh##priorspec) and [<var class="command">paramref</var><strong></strong>](bayesmh##paramref) are defined in [<strong>[BAYES]</strong> bayesmh](http://www.stata.com/help.cgi?bayesmh). |     |     |
| `paramref` may contain factor variables; see [<strong>fvvarlist</strong>](http://www.stata.com/help.cgi?fvvarlist).                                                                                                                                                                                       |     |     |
| See [<strong>[BAYES]</strong> bayesian postestimation](http://www.stata.com/help.cgi?bayesian_postestimation) for features available after estimation.                                                                                                                                                    |     |     |
| Model parameters are regression coefficients `{c -(}depvar1:indepvars{c )-}`, `{c -(}depvar2:indepvars{c )-}`, and so on, and covariance matrix `{c -(}Sigma,matrix{c )-}`. Use the `dryrun` option to see the definitions of model parameters prior to estimation.                                                  |     |     |
| Multivariate Jeffreys prior, `jeffreys(d)`, is used by default for the covariance matrix of dimension `d`.                                                                                                                                                                                                                           |     |     |
| For a detailed description of `bayesopts`, see [<var class="command">Options</var><strong></strong>](bayes##options) in [<strong>[BAYES]</strong> bayes](http://www.stata.com/help.cgi?bayes).                                                                                 |     |     |
# Ideas

> List of potential project ideas.

Before working on your GSoC application, please review our list of ideas to see if you find a project which excites you. The list of existing ideas is provided to serve as inspiration and to indicate which directions may be good for stdlib.

If you do find an existing idea that you'd like to pursue, please be sure to contact us over [Gitter](https://gitter.im/stdlib-js/stdlib) to discuss it first! **Always be sure to ask about these ideas prior to working on application in order to get the latest information about what is already implemented and what exactly must be done.**

Priority, difficulty, technology, and topic area have no bearing on the chances of an idea being accepted. All ideas are equally good, and your chances of being accepted depend solely on the **quality of your application**.

**Project Length**

GSoC allows two different project lengths: **175** hours and **350** hours. Each idea must indicate whether the idea is a better fit for 175 or 350 hours.

In some cases, we may be able to extend a 175 hour project to a 350 hour project by extending the ideas of what can be done. Similarly, in some cases, a 350 hour project can be shortened to a 175 hour project by only implementing part of an idea and leaving the rest for a future project. In either case, if you want to adjust the project length, please be sure to contact us over [Gitter](https://gitter.im/stdlib-js/stdlib) to discuss it first!

## Your Own Idea

If you'd like to submit your own idea, that is also welcome; just be sure to propose your idea to stdlib mentors first! After reaching out, we'll inform you whether the idea has already been implemented, if the idea will entail enough work to last the duration of the GSoC program, if the idea requires too much work to be meaningfully pursued during GSoC, and if the idea is within the scope of stdlib. **Unsolicited, undiscussed ideas are less likely to get accepted.**

The best project for you is the one you are most interested in and knowledgeable about. Excitement and aptitude are two key ingredients of a successful project and help ensure your commitment and ability to see a project through to completion. So if there is something you are especially passionate about and that you believe aligns with the scope and goals of stdlib, we'd be happy to hear your pitch!

After discussing with us over [Gitter](https://gitter.im/stdlib-js/stdlib) and receiving approval to submit your idea, please open an [issue](https://github.com/stdlib-js/google-summer-of-code/issues/new?assignees=&labels=idea&template=idea.yml&title=%5BIdea%5D%3A+) which describes your idea using the [**idea issue template**](https://github.com/stdlib-js/google-summer-of-code/issues/new?assignees=&labels=idea&template=idea.yml&title=%5BIdea%5D%3A+).

* * *
## Building a better Node.js REPL

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/1>

### Idea

The read-eval-print loop (REPL) is a fixture of data analysis and numerical computing and provides a critical entry-point for individuals seeking to learn and better understand APIs and their associated behavior. While a web browser's JavaScript console is a staple of debugging in web applications, the Node.js REPL is significantly underutilized--an occurrence largely attributable to its underdevelopment and lack of functionality.

This idea aims to implement a suite of enhancements to the stdlib REPL, which is an alternative to the Node.js REPL and analogous to Python's IPython. The overarching goal is to provide a compelling environment for interactive JavaScript computing to further establish Node.js as a platform suitable for numerical computing and data analysis.

### Expected Outcomes

REPL users will be able to leverage the stdlib REPL in a manner similar to a fully-featured IDE and have access to workshops and tutorials for an integrated interactive learning experience covering machine learning and statistical computing concepts.

### Involved Software

No other software is necessary to implement this idea.

### Prerequisite Knowledge

JavaScript, Node.js

### Difficulty

Intermediate. Difficulties may arise due to escape sequences necessary for syntax highlighting and multi-line editing.

### Project Length

350 hours.
* * *
## Implement a broader range of statistical distributions

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/2>

### Idea

The goal of this idea is to implement all distributions found in SciPy [stats](https://docs.scipy.org/doc/scipy/tutorial/stats.html). Distribution support will entail implementing APIs for computing PDFs, CDFs, quantiles, and other distribution properties. Additionally, stdlib should support APIs for drawing random variates from any implemented distributions.

### Expected Outcomes

stdlib users will be able to construct, and compute various properties of, every statistical distribution present in SciPy in JavaScript.

### Involved Software

No runtime dependencies should be necessary. SciPy will be necessary in order to provide reference test results.

### Prerequisite Knowledge

JavaScript, Node.js. Familiarity with C/C++/Fortran would help.

### Difficulty

Intermediate. Difficulties may arise for distributions whose properties and moments have complicated formulations. Developing JavaScript implementations will likely require consulting C/C++ and possibly Fortran code.

### Project Length

350 hours.
* * *
## Provide APIs for computing Fast Fourier Transforms

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/3>

### Idea

The goal of this idea is to expose a set of FFT interfaces similar to those available in NumPy and as documented in the Data APIs Array API specification. Similar to stdlib's BLAS interfaces, we may want to allow switching out the FFT backend.

### Expected Outcomes

stdlib users would be able to evaluate FFT operations on stdlib ndarrays. Ideally, we'd also provide a set of C APIs.

### Involved Software

Will need to consult reference implementations in C/Fortran.

### Prerequisite Knowledge

JavaScript, Node.js, C/C++/Fortran

### Difficulty

Hard. This may be a straightforward port, or it may not be. More R&D is needed.

### Project Length

350 hours.
* * *
## Developer dashboard for tracking ecosystem build failures

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/4>

### Idea

The goal of this idea is to build a developer dashboard to display in real-time standalone repository build failures. We currently have the backend database which collects build results in real-time; however, we have yet to build a frontend for viewing and analyzing such data.

### Expected Outcomes

stdlib developers will be able to navigate to a webpage and see the build status for all repositories at once.

### Involved Software

This will involve building a frontend application and interfacing with a backend for querying a PostgreSQL database. We may want to try more "cutting edge" technology here, such as ESBuild, tailwind, etc.

### Prerequisite Knowledge

JavaScript, Node.js, CSS, HTML, JSX.

### Difficulty

Intermediate. Requires a fair amount of frontend engineering knowledge and modern frontend application development.

### Project Length

175/350 hours. A skilled contributor may be able to execute on this faster. If so, scope could be expanded to include analytics and historical overviews.
* * *
## Expand support for additional pseudorandom number generators

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/5>

### Idea

The goal of this idea is to implement a variety of PRNGs for use within stdlib to generate pseudorandom numbers. The project currently uses Mersenne Twister as its default PRNG; however, this PRNG, while common, is not ideal given its comparatively large internal state. Would be great to have a collection of PRNGs, such as PCG, Philox, Xorshift, and more.

### Expected Outcomes

stdlib users will have a wide selection of PRNGs from which to choose from based on their individual needs and considerations. Having a large selection of PRNGs will useful when replicating the results of numerical simulations which may use a PRNG which is not one of the currently supported stdlib PRNGs. Additionally, a desired outcome would be if we could replace MT19937 with a new default PRNG.

### Involved Software

No other software should be necessary. We may be a bit constrained based on 32-bit limitations in JS. This would not, however, stop us from implementing in C for use in generating arrays of random numbers.

### Prerequisite Knowledge

JavaScript, Node.js. Familiarity with C/C++/Fortran would help.

### Difficulty

Intermediate/Hard. Depends. Some PRNGs may be straightforward to implement. Others, not so much.

### Project Length

175/350 hours. This idea can be adjusted according to needs and availability.
* * *
## Add support for visualizing benchmark results

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/6>

### Idea

While we currently support running benchmarks, we have yet to provide a means for easily visualizing and comparing benchmark results. Previously, when wanting to visualize and compare benchmark results, one has needed to manually parse TAP results and then plug into some other software (e.g., vega or Plotly).

The idea for this project would be to 1) implement a TAP parser with support for the latest TAP specification and 2) provide a plot frontend for consuming parsed TAP results. The plot frontend could be as simple as a Unicode bar chart plotter, which would be in line with our existing Unicode plotting facilities.

### Expected Outcomes

Developers will be able to run benchmarks and visually compare benchmark results based on the namespace and parameterization. Ideally, the plot would include small multiple/facet visualizations.

### Involved Software

No other software or dependencies should be necessary. Will need to consult a reference TAP parser implementation (e.g., `node-tap`).

### Prerequisite Knowledge

JavaScript and Node.js.

### Difficulty

Intermediate.

### Project Length

350 hours.
* * *
## Develop a project test runner

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/7>

### Idea

Currently, stdlib uses `tape`. The goal of this idea is to migrate away from `tape` and develop a test runner in-house, similar to `@stdlib/bench/harness`. This has long been on our TODO list and would allow us to have a simple test runner which is oriented toward stdlib conventions (e.g., we don't use most of the assertion methods in `tape`).

Bonus points if we can migrate away from `istanbul` to `nyc` or `c8`; however, this may be tricky if we want to support older Node.js versions.

### Expected Outcomes

All unit tests have migrated to the in-house runner.

### Involved Software

No additional runtime deps. Will need to consult `tape` as a reference implementation, along with our existing `@stdlib/bench/harness` implementation.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate.

### Project Length

175/350 hours. The scope of this idea can be adjusted depending on availability.
* * *
## Reimagine the stdlib plot API and implementation

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/8>

### Idea

Currently, stdlib has a bespoke plot API which is useful for fast static rendering. However, our implementation is quite limited in the types of plots it can produce. The goal of this idea is to refactor our plot API to build atop of `vega` (or its specifications). For this, we'd need to migrate to an async plot generation API, which is probably necessary regardless if we want to support WebGL or some other async rendering engine.

Ideally, we would retain the same plot API and internally generate a vega specification.

### Expected Outcomes

We can generate simple plots using the new plot implementation.

### Involved Software

This will involve using `vega` (or something similar depending on whether `vega` is sufficiently maintained). We will want to transpile to ES5 and vendor in order to ensure that we can support our supported Node.js versions.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate/Hard.

### Project Length

350 hours. This project has the potential to spiral out of control, as there are many unknowns we'd need to answer. Mentor would likely need to be actively involved in order to perform R&D and properly scope.
* * *
## Achieve feature parity with async.js

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/9>

### Idea

Currently, stdlib has a limited set of dedicated "async" APIs for performing various utility operations. The goal of this idea is to achieve feature parity with `async.js`.

### Expected Outcomes

stdlib will have more or less 1:1 feature parity with `async.js` APIs.

### Involved Software

`async.js` will serve as a reference implementation for API design. Will want to modify to match stdlib conventions.

### Prerequisite Knowledge

JavaScript.

### Difficulty

Beginner. Would benefit from someone with JavaScript experience.

### Project Length

175/350 hours. Can be scoped accordingly.
* * *
## Achieve feature parity with builtin Node.js `fs` module

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/10>

### Idea

Achieve feature parity with Node.js `fs` package. We currently only support a limited selection of `fs` methods. Would be useful to support more.

Part of this work involves providing an abstraction layer of Node.js built-ins in order to support newer functionality (e.g., options and/or behavior) not present in older Node.js versions. This is similar in concept to the userland `readable-stream` package.

### Expected Outcomes

stdlib will have complete feature parity with Node.js built-ins.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate. Could require some creative solutions to ensure that abstractions work for older Node.js versions.

### Project Length

175/350 hours. Can be scoped accordingly.
* * *
## Add support for the multivariate normal distribution

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/11>

### Idea

The goal of this idea is to implement the multivariate normal distribution. This distribution is fundamental in a wide variety of statistical applications and will help unblock stdlib in offering additional statistics APIs.

### Expected Outcomes

Users will be able to evaluate the PDF, CDF, logPDF, and logCDF and be able to draw random variates from a specified distribution.

### Involved Software

No other software is necessary. Will require reading reference implementations written in Python, R, and Julia.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate.

### Project Length

175/350 hours. Can be scoped accordingly. A skilled contributor should be able to complete in 175 hours with the potential of using their implementation to implement higher order statistics APIs.
* * *
## Migrate stdlib to use ESLint for linting TypeScript files

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/12>

### Idea

Currently, stdlib uses tslint to lint TypeScript files; however, this utility is now deprecated. The goal of this idea is to migrate stdlib away from tslint to use ESLint for linting. We already use ESLint for linting JavaScript, and being able to use the same linter for TypeScript files would be a significant development improvement, given stdlib's investment in developing custom ESLint rules for enforcing project conventions.

### Expected Outcomes

Linting of stdlib's TypeScript files will be performed by ESLint.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Beginner/Intermediate. 

### Project Length

175/350 hours. Can be scoped accordingly. Scope can be expanded to create custom ESLint rules to enforce particular aspects of stdlib conventions.
* * *
## Develop a Google Sheets extension which exposes stdlib functionality

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/13>

### Idea

The goal of this idea is to allow users to call stdlib APIs from within Google Sheets. This will allow users to perform linear algebra and various machine learning operations directly on spreadsheet data and all within the browser.

### Expected Outcomes

Google Sheets users will be able to install an add-on which exposes stdlib functionality, run statistical tests, evaluate mathematical functions, and perform linear algebra operations using stdlib.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Beginner/Intermediate. 

### Project Length

175/350 hours. Can be scoped accordingly. A skilled contributor can work strategy for performant fused operations.
* * *
## Stdlib API dependency explorer

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/14>

### Idea

The goal of this idea is to provide a visual representation of an API's dependency graph directly in the stdlib API documentation. Initial thinking is that would be an interactive network diagram in which nodes present package dependencies and allow for navigation.

### Expected Outcomes

A user will be able to navigate to a package's documentation page, click to display a network graph, and then click on nodes within that graph to explore the documentation of package dependencies.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js, HTML/CSS, JSX.

### Difficulty

Beginner/Intermediate. 

### Project Length

175 hours.
* * *
## Add support for bootstrap and jackknife resampling

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/15>

### Idea

Manually constructing confidence intervals and other statistical properties can be useful when no analytic solution exists. The goal of this idea to implement APIs for bootstrap and jackknife resampling.

### Expected Outcomes

Users will be to resample provided datasets.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Beginner/Intermediate. 

### Project Length

175/350 hours. Can be scoped accordingly. Scope can be expanded to implement different bootstrap algorithms.
* * *
## Develop a Jupyter backend for interfacing with the stdlib REPL

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/16>

### Idea

Jupyter is a dominate force in scientific computing. While some effort has been done to expose JavaScript kernels to Jupyter/JupyterLab, most of these kernels are under-developed or lack numerical functionality.

The goal of this idea would be to develop a Jupyter backend based on stdlib.

### Expected Outcomes

A JupyterLab user will be able to connect to a stdlib kernel and invoke stdlib operations.

### Involved Software

This goal will require interfacing with the Jupyter technology stack, including ZeroMQ and implementing messaging protocols.

### Prerequisite Knowledge

JavaScript, Node.js. Experience with Python would be very helpful.

### Difficulty

Hard.

### Project Length

350 hours. This idea has many unknowns and will be hard to scope.
* * *
## Implement additional statistical tests

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/17>

### Idea

Implement various statistical tests which are not currently implemented in stdlib, but are implemented in other envs such as R, Python (SciPy, statsmodels), Julia, and MATLAB.

### Expected Outcomes

stdlib will have a broader array of statistical tests which can operate on ndarrays.

### Involved Software

No other software should be necessary. However, we will need to do a needs analysis to determine which prerequisite packages/functionality is necessary in order to allow these tests to be implemented (e.g., BLAS, ndarray slicing, etc).

### Prerequisite Knowledge

JavaScript, Node.js. Familiarity with R, Python, C/C++ would be very useful, as will need to consult reference implementations.

### Difficulty

Hard. Depends on the reference implementation requirements and algorithmic difficulty.

### Project Length

350 hours.
* * *
## Generate web documentation from JSDoc comments

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/19>

### Idea

stdlib relies heavily on JSDoc comments to document its source code. Currently, the project has only rudimentary support for generating HTML docs from those comments. The goal of this idea would be to

1. Write an in-house JSDoc parser.
2. Generate HTML documentation from the parsed comments which is capable of supporting project conventions and its embrace of radical modularity.

### Expected Outcomes

In addition to the current API documentation, a user will be able to navigate to a package's JSDoc documentation to gain more insight into supported input and output dtypes and implemented algorithms. This would be especially useful for rendering the extended JSDoc comment of elementary mathematical functions.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js, HTML/CSS.

### Difficulty

Intermediate.

### Project Length

350 hours.
* * *
## Refactor generated TypeScript interface documentation

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/20>

### Idea

Currently, stdlib publishes TypeScript interface documentation in its web-based API documentation. The generated documentation monkey-patches `tsdoc` to handle generating documentation across the entire mono-repo. The goal of this project is to refactor/rethink this approach and provide a solution capable of addressing the unique constraints of the stdlib project.

### Expected Outcomes

At a base level, it would be great if we had a working documentation render which did not require monkey-patching. A more difficult, but potentially more desirable, outcome would be if TypeScript documentation was not rendered as a separate website, but rather was integrated within the docs as simply another page/fragment.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js, HTML/CSS, TypeScript, JSX/React.

### Difficulty

Intermediate.

### Project Length

175/350 hours. Length will depend on the nature of the proposed solution (e.g., needing to write a custom TypeScript parser vs modifying the existing tsdoc library).
* * *
## Use ES6 modules for running unit tests and benchmarks in web browsers

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/21>

### Idea

Currently, when generating stdlib API documentation, we generate UMD bundles for unit tests and benchmarks. When a user navigates to our package documentation, they can load unit tests and benchmarks and have those run without needing to setup a local environment. The pain point here is that creating separate bundles for each package is time consuming and adds significant heft to the `www` repo.

The goal of this idea is to refactor the way we support unit tests and benchmarks to use ES6 modules and potentially skip bundling altogether. This has the downside of not supporting older browsers which don't support the `<module>` tag, but is probably fine considering that running package unit tests and benchmarks is likely a forward looking concern.

### Expected Outcomes

Users will be able to run unit tests and benchmarks directly in their web browsers by navigating to project API documentation and what is loaded are ES6 modules, not UMD bundles.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js, HTML/CSS, JSX/React.

### Difficulty

Intermediate.

### Project Length

350 hours.
* * *
## Migrate web API documentation to use matomo and instrument for better understanding user navigation behavior

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/22>

### Idea

Currently, the stdlib web-based API docs use GA for analytics and have only minimal integration. E.g., the API docs application is a SPA which uses React and the app does not record changes in page views; we only record first hits.

The goal of this idea is to migrate to using matomo and take advantage of its privacy features. The work will involve instrumenting the API documentation application and integrating with matomo. A potential stretch goal would be to setup dashboards for reporting so that we can better understand user behavior and continue to improve project documentation.

### Expected Outcomes

All user interaction data is logged to matomo and stored in a hosted database.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js, HTML/CSS, JSX/React.

### Difficulty

Intermediate.

### Project Length

350 hours. Can be adjusted depending on skill and ability.
* * *
## Improve the REPL presentation framework

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/23>

### Idea

stdlib currently offers a REPL presentation framework for authoring presentations for use directly in the REPL. This is particularly use for creating interactive tutorials illustrating how to use stdlib functionality for data analysis and visualization from the terminal. Some functionality is missing which would be quite useful. E.g.,

- ASCII plotting
- ASCII animations
- syntax highlighting
- pretty printing tables
- speaker notes
- multiplexing
- theming

### Expected Outcomes

The REPL presentation framework will have additional features similar to those in WYSIWYG presentation applications.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate.

### Project Length

175/350 hours. Can be scoped according to project length.
* * *
## Functions for numerical integration and differentiation

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/24>

### Idea

The goal of this idea is to add functions for numerical integration or differentiation to stdlib as building blocks for downstream algorithms. The functions could be ported from permissively licensed open-source libraries in other languages such as C or Fortran or alternatively be implemented from scratch by consulting the literature and reference implementations from various languages.

### Expected Outcomes

stdlib will have a range of robust functions for performing numerical integration or differentiation

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, Node.js.

### Difficulty

Intermediate.

### Project Length

350 hours.
* * *
## Symbolic Math

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/25>

### Idea

The goal of this idea is to add basic support for symbolic math operations in stdlib.

### Expected Outcome

Users have the ability to perform basic symbolic math operations in JavaScript, such as solving equations, simplifying expressions, and using mathematical functions.

### Involved Software

No other software should be necessary.

### Prerequisite Knowledge

JavaScript, Node.js, and an understanding of mathematics and calculus.

### Difficulty

Intermediate

### Project Length

350 hours.
* * *
## Make code blocks on website documentation interactive

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/26>

### Idea

Currently, all code blocks in the documentation at https://stdlib.io/docs/api/latest is static. To make example code more useful and engaging, it would be nice to have interactive code shells on the website that could be edited and would provide real-time return annotations.

### Expected Outcomes

Improved user experience on the website, as the code examples would become editable and interactive. Return annotations would have to update in real-time, and additional contextual help could be provided via overlays etc. Another outcome would be to make it easy to switch between ES5 and ES6 for code blocks.

### Involved Software

No other software is necessary.

### Prerequisite Knowledge

JavaScript, HTML/CSS, React + JSX

### Difficulty

Hard.

### Project Length

350 hours.
* * *
## Optimization Algorithms

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/27>

### Idea

We currently do not have optimization algorithms in stdlib. Having support for Linear Programming, Convex Optimization, Quadratic Programming, and/or Non-Linear Optimization algorithms would be a great addition.

### Expected Outcomes

stdlib will have a broad array of optimization algorithms for solving problems.

### Involved Software

No other software should be necessary. However, we will need to do a needs analysis to determine which prerequisite packages/functionality is necessary in order to allow these algorithms to be implemented (e.g., BLAS).

### Prerequisite Knowledge

JavaScript, Node.js. Familiarity with R, Python, C/C++ would be very useful, as will need to consult reference implementations.

### Difficulty

Hard. Depends on the reference implementation requirements and algorithmic difficulty.

### Project Length

350 hours.
* * *
## Linear Algebra Functionality

Linked issue: <https://github.com/stdlib-js/google-summer-of-code/issues/28>

### Idea

Currently, support for linear algebra operations in stdlib is limited. The goal of this idea would be to implement algorithms for linear algebra operations such as matrix multiplication, calculating the matrix inverse, eigenvalue calculation, singular value decomposition, Cholesky & LU Decomposition, and the like. This overlaps with the goal of increasing the amount of BLAS and LAPACK that is available in stdlib.

### Expected Outcomes

stdlib will have extended support for linear algebra operations which can be used to solve problems involving matrices and vectors.

### Involved Software

No other software should be necessary. However, we will need to do a needs analysis to determine which prerequisite packages/functionality is necessary in order to allow these operations to be implemented (e.g., BLAS, ndarray slicing, etc).

### Prerequisite Knowledge

JavaScript, Node.js. C, Fortran. Familiarity with linear algebra would be very useful, as will need to consult and understand reference implementations.

### Difficulty

Hard. Depends on the reference implementation requirements and algorithmic difficulty.

### Project Length

350 hours.
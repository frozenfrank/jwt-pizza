# Curiosity Report

The following are a some of the curiosity projects I have undertaken
over the course of this semester. Conveniently, they are mostly
logged and accessible via GitHub Pull Requests or Issues.

## Grading Expectations

I expect that each of these points individually would fulfill the
"curiosity report" requirements, but here I have collected many of them.

Minimal efforts have been spent here to present the information cleanly;
however, each of the individual items are clearly presented as a PR or issue
or commit with supporting resources, links, and arguments for the acceptance
of the item.

##  Deep Dive Projects

- [How can we protect against arbitrary code execution attacks from our dependency on a 3rd party GitHub action?](https://github.com/devops329/devops/pull/95#issue-2641426967)

- [What would it take to migrate to the official `actions/create-release` GitHub action?](https://github.com/devops329/devops/pull/95#issuecomment-2487688517)

- How do I resolve unexpected ESLint errors?
    - [PR](https://github.com/devops329/devops/issues/107)
    - [Resource](https://eslint.org/docs/latest/use/configure/migration-guide#ignoring-files)

- How to generate a chart showing log volume of various error types, assuming low cardinality. Result pictured below.
    ```logql
    sum by (message) (count_over_time({component=~"jwt-pizza-service.*", type="unhandledError"} | json | line_format `{{.message}}` [$__auto]))
    ```
    ![Image](https://github.com/user-attachments/assets/ac051f10-569d-4b16-8b6e-aa219b7d54ef)

- How do I use TS generics to cleanly represent similar shapes, but modify the prefixes on the keys of the objects?
    - [Typing](https://github.com/frozenfrank/jwt-pizza-service/commit/1c4b6b1c125d33b1a6fdbca7adddbd36d9c103da)
    - [Implementation](https://github.com/frozenfrank/jwt-pizza-service/commit/1da322e6494e4f418e5ad5a6e560f41d7170e990)
    - [Resource](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html#key-remapping-via-as)

- Can I track unique sessions separate from the mere active users?
    - Commits: [17b4e73](https://github.com/frozenfrank/jwt-pizza-service/commit/17b4e73fc676185918866e4b28cf7db578675baf), [1da322](https://github.com/frozenfrank/jwt-pizza-service/commit/1da322e6494e4f418e5ad5a6e560f41d7170e990), [1c4b6b](https://github.com/frozenfrank/jwt-pizza-service/commit/1c4b6b1c125d33b1a6fdbca7adddbd36d9c103da)
    - ![Image](https://github.com/user-attachments/assets/dc716ef2-bd71-48a8-b974-3916ffa9ca7e)

## External Curiosity Endeavors

- [Mandelbrot Fractal Calculation](https://github.com/frozenfrank/byu-cs324/blob/master/11a-hw-openmp/RESULTS.md)
    - Went beyond minimum requirements to satisfy my personal curiosity.
    - Learned to use LaTeX expressions for mathematical expressions
    - Gathered my raw data into tables, and then generated a pretty chart to visualize it
    - Wrote a lab-report style summary to introduce my extended family to the problem at hand.

- [What is the most efficient way to guard the `main` branch of organization repos?](https://github.com/softwareconstruction240/softwareconstruction/issues/165)

- [Submitted a well-researched and documented issue to Grafana](https://github.com/grafana/grafana/issues/97386)

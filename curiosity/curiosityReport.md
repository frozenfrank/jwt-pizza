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

- [Mandelbrot Fractal Calculation](./mandelbrot-fractal-evaluations.md)
    - Went beyond minimum requirements to satisfy my personal curiosity.
    - Learned to use LaTeX expressions for mathematical expressions
    - Gathered my raw data into tables, and then generated a pretty chart to visualize it
    - Wrote a lab-report style summary to introduce my extended family to the problem at hand.
    - I have **included a copy of this extra writeup** here because the instructor requested the repository to be private. _The copy was created from commit `afd0a4c`._ View the [source file](https://github.com/frozenfrank/byu-cs324/blob/master/11a-hw-openmp/RESULTS.md).

- [What is the most efficient way to guard the `main` branch of organization repos?](https://github.com/softwareconstruction240/softwareconstruction/issues/165)

- [Submitted a well-researched and documented issue to Grafana](https://github.com/grafana/grafana/issues/97386)

## Class Contributions

Over the course of the semester, I have submitted many PRs with varying quantities of changes.
Some of the PRs have single commits with simple typos, and others have more extensive contributions.

Each of the following issues, PRs, and commits represent work above and beyond the minimal requirements
of my own projects to contribute to a better future for other students. They were all contributed
freely of my own accord, out of a desire to help other students.

The highlighted contributions feature either an application of prior knowledge or a curiosity dive
into related material in order to present an acceptable change for future semesters.
For example, hardening the `github-ci` IAM rights required reading through AWS documentation
pages and other examples to figure out what the minimal required set of permissions should be
to still function properly.

Note that some of these may have been referred to in whole or in party by the [Deep Dive projects](#deep-dive-projects) section above.

* **TOTAL** (organization: `devops329`)
  * [**23 merged PRs**](https://github.com/search?q=org%3Adevops329+is%3Apr+is%3Amerged+author%3Afrozenfrank&type=pullrequests)
  * [28 total PRs](https://github.com/search?q=org%3Adevops329+author%3Afrozenfrank&type=pullrequests)
  * [6 issues](https://github.com/search?q=org%3Adevops329+author%3Afrozenfrank&type=issues)
  * [39 commits](https://github.com/search?q=org%3Adevops329+author%3Afrozenfrank&type=commits)
* Instructions (`devops329/devops`)
  * [**21 merged PRs**](https://github.com/devops329/devops/pulls?q=author%3Afrozenfrank+is%3Amerged), 26 total
  * [6 total issues](https://github.com/devops329/devops/issues?q=is%3Aissue+author%3Afrozenfrank+), 5 completed and 1 still open
  * Highlights
    * [Adjust Grafana Instruction Pages](https://github.com/devops329/devops/pull/102)
    * [Resolve 3rd party action security hole](https://github.com/devops329/devops/pull/95)
    * [Harden github-ci IAM rights (tested)](https://github.com/devops329/devops/pull/94)
    * [Update awsEcr.md Provide Provenance flag to avoid "three artifact" behavior](https://github.com/devops329/devops/pull/90)
    * [Update jwtPizzaServiceContainer.md Refer to Docker image by tag](https://github.com/devops329/devops/pull/76)
* JWT Pizza client (`devops329/jwt-pizza`)
  * [**1 merged PR**](https://github.com/devops329/jwt-pizza/pulls?q=author%3Afrozenfrank+)
  * Highlight:
    * [Exclude .vite from .gitignore](https://github.com/devops329/jwt-pizza/pull/5)
* JWT Pizza server (`devops329/jwt-pizza-service`)
  * [**1 merged PR**](https://github.com/devops329/jwt-pizza-service/pulls?q=author%3Afrozenfrank+)
  * Highlight:
    * [Properly await clearAuth() request](https://github.com/devops329/jwt-pizza-service/pull/6)

## Total Time Spent

I use a time logging app called Toggl.com for my own personal time accountability.
I use it to track my time really closely as I switch between projects, classes,
and other adventures. The result is a very accurate representation of the total
time I spent on the different portions of this class.

View my [CS 329 Total Time Report](./img/CS_329_Toggle_Time_Report.pdf).

Note the following details of the reported data:
* The timestamps really are precise down to the second, and I accurately logged them as I started and stopped each time block.
* Stopping at Dec 8th, 2024, this report excludes the authorship of this Curiosity Report and any other final conclusions to the semester. It does include the serious majority of all work performed in connection to this class.
* All _homework assignments_ were grouped together under the same title ("Homework")
* Each _deliverable_ was tracked under a separate title, but some deliverables may be spread across multiple titles to track major phases of the work.
* I separated out some of my time on deeper dive projects and curiosity items into the "Curiosity" title, but no very well. Significant portions of the "Homework" and "Deliverable 8 — Metrics" titles may actually included time spent working on things not strictly required to pass the assignment.
* I fell behind during the semester and spent a serious amount of time catching up over Thanksgiving week.
* The report has some unnecessary and redundant information because it is capable of supporting other use cases. Mostly just pay attention to:
  * Time series on the first page.
  * The "Time Entry" pie chart and associated legend showing total times for each entry

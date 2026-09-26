# Repository agent guide

## Repository workflow and completion

The Go application implements Terraform PR automation; `runatlantis.io/` is the documentation site. `go.mod` requires Go 1.25.4, newer than the `.tool-versions` Go entry; resolve this before tests. Use the npm lockfile for website dependencies. `make test` runs short Go tests, `make test-all` broadens coverage, `make lint` runs golangci-lint, and `make check-fmt` checks formatting. `make build` targets Linux/amd64.

Website scripts are `website:dev`, `website:lint`, and `website:build`. Follow `CONTRIBUTING.md` and retain its DCO sign-off requirement. Use isolated repos/fake credentials. Starting Atlantis, Terraform plans/applies, hooks, and live GitHub/infrastructure contact require corresponding authorization. Unit success does not prove an infrastructure plan or deployment.

Continue the authorized change through relevant validation and repair of failures it causes; preserve unrelated work. Report checks actually run, commands only inspected, and exact missing prerequisites. Ask only when a material decision, missing authorization, or required input blocks progress; continue independent reversible work. Existing mandatory contribution and validation gates still apply.

---
title: Development
description: The tooling behind the repo and how to set it up locally.
---

```bash
./setup       # install mise and setup repository
mise run      # run tasks interactively
```

| Feature                                        | With                                                                                   | Configuration                                                                                                 |
| ---------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Continuous Integration                         | [GitHub Workflow](https://docs.github.com/en/actions/using-workflows)                  | [.github/workflows](https://github.com/espadat-studio/colporteur/tree/master/.github/workflows)               |
| Conventional Commits                           | [convco](https://github.com/convco/convco)                                             | [.convco](https://github.com/espadat-studio/colporteur/blob/master/.convco)                                   |
| Conventional PR Titles                         | [action-semantic-pull-request](https://github.com/amannn/action-semantic-pull-request) | [semantic-pr.yml](https://github.com/espadat-studio/colporteur/blob/master/.github/workflows/semantic-pr.yml) |
| Documentation                                  | [Starlight](https://starlight.astro.build/)                                            | [docs/](https://github.com/espadat-studio/colporteur/tree/master/docs)                                        |
| Formatting                                     | [dprint](https://dprint.dev/)                                                          | [.dprint.jsonc](https://github.com/espadat-studio/colporteur/blob/master/.dprint.jsonc)                       |
| Git Hooks                                      | [hk](https://hk.jdx.dev/)                                                              | [hk.pkl](https://github.com/espadat-studio/colporteur/blob/master/hk.pkl)                                     |
| Tasks Runner, Environment & Runtime Management | [mise](https://mise.dev/)                                                              | [mise.toml](https://github.com/espadat-studio/colporteur/blob/master/mise.toml)                               |

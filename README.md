# djp-template

A [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) jsonnet package (**djp**).

## Description

[OWASP Dependency Check](https://owasp.org/www-project-dependency-check/) **djp** package.

## Snippet

- `ddb.yml`

```yaml
cookiecutter:
  templates:
    - template: gh:inetum-orleans/djp-owasp-dependency-check
```

- `docker-compose.yml.jsonnet`

```jsonnet
ddb.Compose(
  ddb.with(
    import '.docker/djp-owasp-dependency-check/djp.libjsonnet',
    params={global: true, args: ['--format ="\ALL\" --enableExperimental']}
  )
)
```

## Parameters

| name  | type | description |
| ------------- | ------------- | ------------- |
| global  | boolean  | Should the binary be global ?
| args  | string  | Additional arguments for dependency-check

## Usage

Please check [jsonnet feature](https://inetum-orleans.github.io/docker-devbox-ddb/features/jsonnet/#ddb-jsonnet-packages-djp)
to understand how to include a **djp** package inside a [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) project.

Looking for other [djp packages](https://github.com/inetum-orleans?q=djp-) ? Check github repositories starting with `djp-`.

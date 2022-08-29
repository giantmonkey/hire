---
title: Semantic version comparison
layout: home
---

## Your task:
Implement a ruby class `Semver` that can be used to compare semantic versions. 

Your class should support the operators `<`, `>` and `==`. It should also implement a `#match?` method that matches against Gemfile version strings like `'~> 10.1'`.

### Examples
```
Semver.new('1.10') > Semver.new('2.10')   # => false
Semver.new('1.10') < Semver.new('2.10')   # => true

Semver.new('1.10') == Semver.new('1.10')  # => true

Semver.new('1.9.1').match?('~> 1.10')     # => false
Semver.new('1.10.1').match?('~> 1.10')    # => true
Semver.new('1.10.1').match?('> 1.10')     # => true
```

## What we are looking for:
* Process of working documented by concise commits
* Clean, readable code
* Tests!

## Recommended time
2 - 4 hours

# flutter_example

### 一、代码规范：
https://mp.weixin.qq.com/s/aQyRLaszBAmcs63eCYXZXA

#### 1、代码美化
```
 dartfmt -w --fix lib/
```

#### 2、代码质量检查
pubspec.yaml 中配置
```
dependencies:
  flutter:
    sdk: flutter

  pedantic: ^1.8.0

  cupertino_icons: ^0.1.3

dev_dependencies:
  flutter_test:
    sdk: flutter
  pedantic: ^1.8.0

```

配置 analysis_options.yaml

```
include: package:pedantic/analysis_options.1.8.0.yaml
analyzer:
  strong-mode:
    implicit-casts: false
linter:
  rules:
    - camel_case_types
    - camel_case_extensions
    - file_names
    - non_constant_identifier_names
    - constant_identifier_names # prefer
    - directives_ordering
    - lines_longer_than_80_chars # avoid
    - package_api_docs # prefer
    - public_member_api_docs # prefer
```

使用
```
dartanalyzer lib

```
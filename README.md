# flutter_dependabot_example

This project demonstrates that dependabot is not useable for Flutter projects using the beta channel.

This problem is tracked at https://github.com/dependabot/dependabot-core/issues/5084

## How to reproduce

### 1. Make sure you are on the Flutter stable channel

```bash
flutter channel stable
```

### 2. Create a new flutter project

```bash
flutter create -h --project-name flutter_dependabot_example --org com.pascalwelsch .
```

### 3. Add `.github/dependabot.yaml`

```yaml
# This is part of the preview program of dependabot for dart
version: 2

enable-beta-ecosystems: true
updates:
  - package-ecosystem: "pub"
    directory: "/"
    schedule:
      interval: "daily"
```

Dependabot should now run (https://github.com/passsy/flutter_dependabot_example/network/updates) without creating any PRs (all up-to-date)


<details>
<summary>Full Output</summary>

```
  proxy | time="2022-04-11T12:06:59Z" level=info msg="proxy starting" commit=0cfe6fc8a85a641097e4d9faf5c8349b892b1e40
  proxy | 2022/04/11 12:06:59 Listening (:1080)
updater | 2022-04-11T12:06:59.352757865 [anonymous-instance:main:WARN:src/firecracker/src/main.rs:370] You are using a deprecated parameter: --seccomp-level 2, that will be removed in a future version.
updater | 2022-04-11T12:06:59.374563413 [339483593:main:WARN:src/devices/src/legacy/serial.rs:432] Detached the serial input due to peer close/error.
updater | time="2022-04-11T12:07:01Z" level=info msg="guest starting" commit=f727200bdf4574dc1f7be439933549abd8d15da9
updater | time="2022-04-11T12:07:01Z" level=info msg="starting job..." fetcher_timeout=5m0s job_id=339483593 updater_timeout=45m0s updater_version=0.180.5-fa5bb09ca507cf1caf68ca73cfd011f9620038d6
updater | I, [2022-04-11T12:07:02.328864 #7]  INFO -- sentry: ** [Raven] Raven 3.1.2 ready to catch errors
updater | INFO <job_339483593> Starting job processing
  proxy | 2022/04/11 12:07:04 [002] GET https://api.github.com:443/repos/passsy/flutter_dependabot_example
  proxy | 2022/04/11 12:07:04 [002] * authenticating github api request
  proxy | 2022/04/11 12:07:04 [002] 200 https://api.github.com:443/repos/passsy/flutter_dependabot_example
  proxy | 2022/04/11 12:07:04 [004] GET https://api.github.com:443/repos/passsy/flutter_dependabot_example/git/refs/heads/main
  proxy | 2022/04/11 12:07:04 [004] * authenticating github api request
  proxy | 2022/04/11 12:07:04 [004] 200 https://api.github.com:443/repos/passsy/flutter_dependabot_example/git/refs/heads/main
  proxy | 2022/04/11 12:07:05 [007] GET https://github.com:443/passsy/flutter_dependabot_example/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:07:05 [007] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:07:05 [007] 200 https://github.com:443/passsy/flutter_dependabot_example/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:07:05 [009] POST https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:07:05 [009] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:07:05 [009] 200 https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:07:05 [011] POST https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:07:05 [011] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:07:05 [011] 200 https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
updater | INFO <job_339483593> Finished job processing
updater | time="2022-04-11T12:07:05Z" level=info msg="task complete" container_id=job-339483593-file-fetcher exit_code=0 job_id=339483593 step=fetcher
updater | I, [2022-04-11T12:07:06.719220 #8]  INFO -- sentry: ** [Raven] Raven 3.1.2 ready to catch errors
updater | INFO <job_339483593> Starting job processing
updater | INFO <job_339483593> Starting update job for passsy/flutter_dependabot_example
updater | INFO <job_339483593> Checking if flutter 0.0.0 needs updating
  proxy | 2022/04/11 12:07:21 [016] GET https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:07:21 [017] GET https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:07:21 [017] 200 https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:07:21 [016] 200 https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:07:21 [019] GET https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:07:21 [019] 200 https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:07:21 [029] GET https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:07:21 [030] GET https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:07:21 [031] GET https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:07:21 [032] GET https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:07:21 [033] GET https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:07:21 [034] GET https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:07:21 [035] GET https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:07:21 [036] GET https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:07:21 [037] GET https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:07:21 [029] 200 https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:07:21 [039] GET https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:07:21 [030] 200 https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:07:21 [035] 200 https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:07:21 [033] 200 https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:07:21 [034] 200 https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:07:21 [032] 200 https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:07:21 [037] 200 https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:07:21 [031] 200 https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:07:21 [036] 200 https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:07:21 [039] 200 https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:07:21 [041] GET https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:07:21 [041] 200 https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:07:21 [046] GET https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:07:21 [050] GET https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:07:21 [051] GET https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:07:21 [052] GET https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:07:21 [053] GET https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:07:21 [054] GET https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:07:21 [055] GET https://pub.dartlang.org:443/api/packages/typed_data
  proxy | 2022/04/11 12:07:21 [057] GET https://pub.dartlang.org:443/api/packages/vector_math
  proxy | 2022/04/11 12:07:21 [046] 200 https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:07:21 [050] 200 https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:07:21 [051] 200 https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:07:21 [053] 200 https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:07:21 [054] 200 https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:07:21 [055] 200 https://pub.dartlang.org:443/api/packages/typed_data
  proxy | 2022/04/11 12:07:21 [052] 200 https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:07:21 [057] 200 https://pub.dartlang.org:443/api/packages/vector_math
updater | INFO <job_339483593> Latest version is 0.0.0
updater | INFO <job_339483593> No update needed for flutter 0.0.0
updater | INFO <job_339483593> Checking if cupertino_icons 1.0.4 needs updating
updater | INFO <job_339483593> Latest version is 1.0.4
updater | INFO <job_339483593> No update needed for cupertino_icons 1.0.4
updater | INFO <job_339483593> Checking if flutter_test 0.0.0 needs updating
updater | INFO <job_339483593> Latest version is 0.0.0
updater | INFO <job_339483593> No update needed for flutter_test 0.0.0
updater | INFO <job_339483593> Checking if flutter_lints 1.0.4 needs updating
updater | INFO <job_339483593> Latest version is 2.0.0
updater | INFO <job_339483593> Requirements to unlock update_not_possible
updater | INFO <job_339483593> Requirements update strategy 
updater | INFO <job_339483593> No update possible for flutter_lints 1.0.4
updater | INFO <job_339483593> Finished job processing
updater | time="2022-04-11T12:07:23Z" level=info msg="task complete" container_id=job-339483593-updater exit_code=0 job_id=339483593 step=updater
```

</details>

### 4. Update flutter to beta channel

```bash
flutter channel beta
```

Update the dependencies that are locked by the Flutter SDK

```bash
flutter pub get
```

This updates `path` (`1.8.0` -> `1.8.1`) and `test_api` (`0.4.8` -> `0.4.9`) because the flutter SDK forces exact versions.

![Screen-Shot-2022-04-11-14-11-24 11](https://user-images.githubusercontent.com/1096485/162736929-54bc484b-fcff-4236-b97f-cc128f50d17d.png)

### 5. Add an outdated dependency


Adding an outdated dependency that will trigger dependabot to update the dependency.
`go_router`s latest version is `3.0.7`, let's add `3.0.5` explicitly.

```
flutter pub add go_router:3.0.5 
```

### 6. Run dependabot (manually)

Trigger dependabot manually to get a automatic PR.

Dependabot detects a new `go_router` version.

```
updater | +---------+-----------------------------------+
updater | |     Changes to Dependabot Pull Requests     |
updater | +---------+-----------------------------------+
updater | | created | go_router ( from 3.0.5 to 3.0.7 ) |
updater | +---------+-----------------------------------+
```

<details>
<summary>Full output</summary>

```
  proxy | time="2022-04-11T12:18:08Z" level=info msg="proxy starting" commit=0cfe6fc8a85a641097e4d9faf5c8349b892b1e40
  proxy | 2022/04/11 12:18:08 Listening (:1080)
updater | 2022-04-11T12:18:08.229555167 [anonymous-instance:main:WARN:src/firecracker/src/main.rs:370] You are using a deprecated parameter: --seccomp-level 2, that will be removed in a future version.
updater | 2022-04-11T12:18:08.255254443 [339496903:main:WARN:src/devices/src/legacy/serial.rs:432] Detached the serial input due to peer close/error.
updater | time="2022-04-11T12:18:09Z" level=info msg="guest starting" commit=f727200bdf4574dc1f7be439933549abd8d15da9
updater | time="2022-04-11T12:18:09Z" level=info msg="starting job..." fetcher_timeout=5m0s job_id=339496903 updater_timeout=45m0s updater_version=0.180.5-fa5bb09ca507cf1caf68ca73cfd011f9620038d6
updater | I, [2022-04-11T12:18:11.236391 #7]  INFO -- sentry: ** [Raven] Raven 3.1.2 ready to catch errors
updater | INFO <job_339496903> Starting job processing
  proxy | 2022/04/11 12:18:13 [002] GET https://api.github.com:443/repos/passsy/flutter_dependabot_example
  proxy | 2022/04/11 12:18:13 [002] * authenticating github api request
  proxy | 2022/04/11 12:18:13 [002] 200 https://api.github.com:443/repos/passsy/flutter_dependabot_example
  proxy | 2022/04/11 12:18:13 [004] GET https://api.github.com:443/repos/passsy/flutter_dependabot_example/git/refs/heads/main
  proxy | 2022/04/11 12:18:13 [004] * authenticating github api request
  proxy | 2022/04/11 12:18:13 [004] 200 https://api.github.com:443/repos/passsy/flutter_dependabot_example/git/refs/heads/main
  proxy | 2022/04/11 12:18:14 [007] GET https://github.com:443/passsy/flutter_dependabot_example/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:14 [007] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:18:14 [007] 200 https://github.com:443/passsy/flutter_dependabot_example/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:14 [009] POST https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:18:14 [009] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:18:14 [009] 200 https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:18:14 [011] POST https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
  proxy | 2022/04/11 12:18:14 [011] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:18:14 [011] 200 https://github.com:443/passsy/flutter_dependabot_example/git-upload-pack
updater | INFO <job_339496903> Finished job processing
updater | time="2022-04-11T12:18:14Z" level=info msg="task complete" container_id=job-339496903-file-fetcher exit_code=0 job_id=339496903 step=fetcher
updater | I, [2022-04-11T12:18:15.727299 #7]  INFO -- sentry: ** [Raven] Raven 3.1.2 ready to catch errors
updater | INFO <job_339496903> Starting job processing
updater | INFO <job_339496903> Starting update job for passsy/flutter_dependabot_example
updater | INFO <job_339496903> Checking if flutter 0.0.0 needs updating
  proxy | 2022/04/11 12:18:31 [017] GET https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:18:31 [018] GET https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:18:31 [019] GET https://pub.dartlang.org:443/api/packages/go_router
  proxy | 2022/04/11 12:18:31 [019] 200 https://pub.dartlang.org:443/api/packages/go_router
  proxy | 2022/04/11 12:18:31 [018] 200 https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:18:31 [017] 200 https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:18:31 [021] GET https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:18:32 [021] 200 https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:18:32 [024] GET https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:18:32 [025] GET https://pub.dartlang.org:443/api/packages/logging
  proxy | 2022/04/11 12:18:32 [024] 200 https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:18:32 [025] 200 https://pub.dartlang.org:443/api/packages/logging
  proxy | 2022/04/11 12:18:32 [033] GET https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:18:32 [034] GET https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:18:32 [035] GET https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:18:32 [036] GET https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:18:32 [037] GET https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:18:32 [038] GET https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:18:32 [039] GET https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:18:32 [033] 200 https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:18:32 [034] 200 https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:18:32 [036] 200 https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:18:32 [035] 200 https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:18:32 [037] 200 https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:18:32 [039] 200 https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:18:32 [038] 200 https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:18:32 [041] GET https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:18:32 [043] GET https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:18:32 [041] 200 https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:18:32 [043] 200 https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:18:32 [045] GET https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:18:32 [045] 200 https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:18:32 [052] GET https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:18:32 [054] GET https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:18:32 [055] GET https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:18:32 [056] GET https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:18:32 [057] GET https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:18:32 [058] GET https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:18:32 [060] GET https://pub.dartlang.org:443/api/packages/typed_data
  proxy | 2022/04/11 12:18:32 [061] GET https://pub.dartlang.org:443/api/packages/vector_math
  proxy | 2022/04/11 12:18:32 [052] 200 https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:18:32 [054] 200 https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:18:32 [056] 200 https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:18:32 [055] 200 https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:18:32 [057] 200 https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:18:32 [058] 200 https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:18:32 [060] 200 https://pub.dartlang.org:443/api/packages/typed_data
  proxy | 2022/04/11 12:18:32 [061] 200 https://pub.dartlang.org:443/api/packages/vector_math
  proxy | 2022/04/11 12:18:32 [063] GET https://pub.dartlang.org:443/api/packages/js
  proxy | 2022/04/11 12:18:32 [063] 200 https://pub.dartlang.org:443/api/packages/js
updater | INFO <job_339496903> Latest version is 0.0.0
updater | INFO <job_339496903> No update needed for flutter 0.0.0
updater | INFO <job_339496903> Checking if cupertino_icons 1.0.4 needs updating
updater | INFO <job_339496903> Latest version is 1.0.4
updater | INFO <job_339496903> No update needed for cupertino_icons 1.0.4
updater | INFO <job_339496903> Checking if flutter_test 0.0.0 needs updating
updater | INFO <job_339496903> Latest version is 0.0.0
updater | INFO <job_339496903> No update needed for flutter_test 0.0.0
updater | INFO <job_339496903> Checking if flutter_lints 1.0.4 needs updating
updater | INFO <job_339496903> Latest version is 2.0.0
updater | INFO <job_339496903> Requirements to unlock update_not_possible
updater | INFO <job_339496903> Requirements update strategy 
updater | INFO <job_339496903> No update possible for flutter_lints 1.0.4
updater | INFO <job_339496903> Checking if go_router 3.0.5 needs updating
updater | INFO <job_339496903> Latest version is 3.0.7
updater | INFO <job_339496903> Requirements to unlock own
updater | INFO <job_339496903> Requirements update strategy 
updater | INFO <job_339496903> Updating go_router from 3.0.5 to 3.0.7
  proxy | 2022/04/11 12:18:37 [066] GET https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:18:37 [067] GET https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:18:37 [067] 200 https://pub.dartlang.org:443/api/packages/lints
  proxy | 2022/04/11 12:18:37 [066] 200 https://pub.dartlang.org:443/api/packages/flutter_lints
  proxy | 2022/04/11 12:18:38 [078] GET https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:18:38 [079] GET https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:18:38 [080] GET https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:18:38 [081] GET https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:18:38 [082] GET https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:18:38 [083] GET https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:18:38 [084] GET https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:18:38 [085] GET https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:18:38 [086] GET https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:18:38 [087] GET https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:18:38 [078] 200 https://pub.dartlang.org:443/api/packages/test_api
  proxy | 2022/04/11 12:18:38 [079] 200 https://pub.dartlang.org:443/api/packages/string_scanner
  proxy | 2022/04/11 12:18:38 [085] 200 https://pub.dartlang.org:443/api/packages/stream_channel
  proxy | 2022/04/11 12:18:38 [084] 200 https://pub.dartlang.org:443/api/packages/meta
  proxy | 2022/04/11 12:18:38 [080] 200 https://pub.dartlang.org:443/api/packages/async
  proxy | 2022/04/11 12:18:38 [087] 200 https://pub.dartlang.org:443/api/packages/source_span
  proxy | 2022/04/11 12:18:38 [083] 200 https://pub.dartlang.org:443/api/packages/stack_trace
  proxy | 2022/04/11 12:18:38 [081] 200 https://pub.dartlang.org:443/api/packages/collection
  proxy | 2022/04/11 12:18:38 [082] 200 https://pub.dartlang.org:443/api/packages/boolean_selector
  proxy | 2022/04/11 12:18:38 [086] 200 https://pub.dartlang.org:443/api/packages/path
  proxy | 2022/04/11 12:18:38 [090] GET https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:18:38 [091] GET https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:18:38 [090] 200 https://pub.dartlang.org:443/api/packages/term_glyph
  proxy | 2022/04/11 12:18:38 [091] 200 https://pub.dartlang.org:443/api/packages/matcher
  proxy | 2022/04/11 12:18:38 [093] GET https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:18:38 [093] 200 https://pub.dartlang.org:443/api/packages/charcode
  proxy | 2022/04/11 12:18:38 [096] GET https://pub.dartlang.org:443/api/packages/go_router
  proxy | 2022/04/11 12:18:38 [097] GET https://pub.dartlang.org:443/api/packages/logging
  proxy | 2022/04/11 12:18:38 [096] 200 https://pub.dartlang.org:443/api/packages/go_router
  proxy | 2022/04/11 12:18:38 [097] 200 https://pub.dartlang.org:443/api/packages/logging
  proxy | 2022/04/11 12:18:38 [099] GET https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:18:38 [099] 200 https://pub.dartlang.org:443/api/packages/cupertino_icons
  proxy | 2022/04/11 12:18:38 [101] GET https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:18:38 [101] 200 https://pub.dartlang.org:443/api/packages/material_color_utilities
  proxy | 2022/04/11 12:18:38 [103] GET https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:18:38 [103] 200 https://pub.dartlang.org:443/api/packages/characters
  proxy | 2022/04/11 12:18:38 [105] GET https://pub.dartlang.org:443/api/packages/vector_math
  proxy | 2022/04/11 12:18:38 [105] 200 https://pub.dartlang.org:443/api/packages/vector_math
  proxy | 2022/04/11 12:18:38 [107] GET https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:18:38 [107] 200 https://pub.dartlang.org:443/api/packages/clock
  proxy | 2022/04/11 12:18:38 [109] GET https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:18:38 [109] 200 https://pub.dartlang.org:443/api/packages/fake_async
  proxy | 2022/04/11 12:18:38 [111] GET https://pub.dartlang.org:443/api/packages/js
  proxy | 2022/04/11 12:18:38 [111] 200 https://pub.dartlang.org:443/api/packages/js
  proxy | 2022/04/11 12:18:39 [113] GET https://api.github.com:443/repos/passsy/flutter_dependabot_example/commits?per_page=100
  proxy | 2022/04/11 12:18:39 [113] * authenticating github api request
  proxy | 2022/04/11 12:18:39 [113] 200 https://api.github.com:443/repos/passsy/flutter_dependabot_example/commits?per_page=100
  proxy | 2022/04/11 12:18:40 [115] GET https://pub.dev:443/api/packages/go_router
  proxy | 2022/04/11 12:18:40 [115] 200 https://pub.dev:443/api/packages/go_router
  proxy | 2022/04/11 12:18:40 [117] GET https://api.github.com:443/repos/flutter/packages/releases?per_page=100
  proxy | 2022/04/11 12:18:40 [117] * authenticating github api request
  proxy | 2022/04/11 12:18:40 [117] 200 https://api.github.com:443/repos/flutter/packages/releases?per_page=100
  proxy | 2022/04/11 12:18:40 [119] GET https://api.github.com:443/repos/flutter/packages/contents/packages
  proxy | 2022/04/11 12:18:40 [119] * authenticating github api request
  proxy | 2022/04/11 12:18:40 [119] 200 https://api.github.com:443/repos/flutter/packages/contents/packages
  proxy | 2022/04/11 12:18:40 [121] GET https://api.github.com:443/repos/flutter/packages/contents/
  proxy | 2022/04/11 12:18:40 [121] * authenticating github api request
  proxy | 2022/04/11 12:18:40 [121] 200 https://api.github.com:443/repos/flutter/packages/contents/
  proxy | 2022/04/11 12:18:41 [123] GET https://github.com:443/flutter/packages.git/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:41 [123] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:18:41 [123] 200 https://github.com:443/flutter/packages.git/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:41 [125] GET https://api.github.com:443/repos/flutter/packages/contents/packages?ref=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [125] * authenticating github api request
  proxy | 2022/04/11 12:18:41 [125] 200 https://api.github.com:443/repos/flutter/packages/contents/packages?ref=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [127] GET https://api.github.com:443/repos/flutter/packages/contents/?ref=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [127] * authenticating github api request
  proxy | 2022/04/11 12:18:41 [127] 200 https://api.github.com:443/repos/flutter/packages/contents/?ref=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [129] GET https://github.com:443/flutter/packages.git/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:41 [129] * authenticating git server request (host: github.com)
  proxy | 2022/04/11 12:18:41 [129] 200 https://github.com:443/flutter/packages.git/info/refs?service=git-upload-pack
  proxy | 2022/04/11 12:18:41 [131] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:41 [131] * authenticating github api request
  proxy | 2022/04/11 12:18:41 [131] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:41 [133] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [133] * authenticating github api request
  proxy | 2022/04/11 12:18:41 [133] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
  proxy | 2022/04/11 12:18:41 [135] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:41 [135] * authenticating github api request
  proxy | 2022/04/11 12:18:42 [135] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:42 [137] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
  proxy | 2022/04/11 12:18:42 [137] * authenticating github api request
  proxy | 2022/04/11 12:18:42 [137] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
  proxy | 2022/04/11 12:18:42 [139] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:42 [139] * authenticating github api request
  proxy | 2022/04/11 12:18:42 [139] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.5
  proxy | 2022/04/11 12:18:42 [141] GET https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
  proxy | 2022/04/11 12:18:42 [141] * authenticating github api request
  proxy | 2022/04/11 12:18:42 [141] 200 https://api.github.com:443/repos/flutter/packages/commits?path=packages&sha=go_router-v3.0.7
updater | INFO <job_339496903> Submitting go_router pull request for creation
updater | INFO <job_339496903> Finished job processing
updater | INFO Results:
updater | +---------+-----------------------------------+
updater | |     Changes to Dependabot Pull Requests     |
updater | +---------+-----------------------------------+
updater | | created | go_router ( from 3.0.5 to 3.0.7 ) |
updater | +---------+-----------------------------------+
updater | time="2022-04-11T12:18:43Z" level=info msg="task complete" container_id=job-339496903-updater exit_code=0 job_id=339496903 step=updater
```

</details>

And dependabot creates a PR https://github.com/passsy/flutter_dependabot_example/pull/1

### Expected Diff

Dependabot only updates go_router

```diff
// pubspec.yaml

- go_router: 3.0.5
+ go_router: ^3.0.5
```

```diff
// pubspec.lock

  go_router:
    dependency: "direct main"
    description:
      name: go_router
      url: "https://pub.dartlang.org"
    source: hosted
-    version: "3.0.5"
+    version: "3.0.7"
```


### Actual Diff

See [PR#1](https://github.com/passsy/flutter_dependabot_example/pull/1/files)

Dependabot downgrades `js`, `path` and `test_api` because dependabot uses an older version of Flutter.

```diff
// pubspec.yaml

- go_router: 3.0.5
+ go_router: ^3.0.7
```

```diff
// pubspec.lock

  go_router:
    dependency: "direct main"
    description:
      name: go_router
      url: "https://pub.dartlang.org"
    source: hosted
-    version: "3.0.5"
+    version: "3.0.7"
  js:
    dependency: transitive
    description:
      name: js
      url: "https://pub.dartlang.org"
    source: hosted
-    version: "0.6.4"
+    version: "0.6.3"
  path:
    dependency: transitive
    description:
      name: path
      url: "https://pub.dartlang.org"
    source: hosted
-    version: "1.8.1"
+    version: "1.8.0"
  test_api:
    dependency: transitive
    description:
      name: test_api
      url: "https://pub.dartlang.org"
    source: hosted
-    version: "0.4.9"
+    version: "0.4.8"
```

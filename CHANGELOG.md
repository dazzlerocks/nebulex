# Changelog

## [v2.0.0](https://github.com/cabol/nebulex/tree/v2.0.0) (2021-02-20)

[Full Changelog](https://github.com/cabol/nebulex/compare/v2.0.0-rc.2...v2.0.0)

**Added features:**

- Added `delete_all/2` and `count_all/2` functions to the Cache API
  [#100](https://github.com/cabol/nebulex/issues/100)
- Added `decr/3` to the Cache API.

**Implemented enhancements:**

- Added `join_cluster` and `leave_cluster` functions to the distributed adapters
  [#104](https://github.com/cabol/nebulex/issues/104)
- Removed `Nebulex.Time.expiry_tine/2`; use `:timer.(seconds|minutes|hours)/1`
  instead.

**Closed issues:**

- Migrating to v2 link is broken
  [#103](https://github.com/cabol/nebulex/issues/103)
- Fixed replicated adapter to work properly with dynamic caches
  [#101](https://github.com/cabol/nebulex/issues/101)

## [v2.0.0-rc.2](https://github.com/cabol/nebulex/tree/v2.0.0-rc.2) (2021-01-06)

[Full Changelog](https://github.com/cabol/nebulex/compare/v2.0.0-rc.1...v2.0.0-rc.2)

**Added features:**

- Added adapter `Nebulex.Adapters.Nil` for disabling caching
  [#88](https://github.com/cabol/nebulex/issues/88)
- Added adapter for `whitfin/cachex`
  [#20](https://github.com/cabol/nebulex/issues/20)

**Implemented enhancements:**

- Improved replicated adapter to ensure better consistency across the nodes
  [#99](https://github.com/cabol/nebulex/issues/99)
- Refactored Nebulex task for generating caches
  [#97](https://github.com/cabol/nebulex/issues/97)
- Added `Nebulex.Adapter.Stats` behaviour as optional
  [#95](https://github.com/cabol/nebulex/issues/95)
- Added `Nebulex.Adapter.Entry` and `Nebulex.Adapter.Storage` behaviours
  [#93](https://github.com/cabol/nebulex/issues/93)
- Added `:default` option to the `incr/3` callback
  [#92](https://github.com/cabol/nebulex/issues/92)
- Fixed `Nebulex.RPC` to use `:erpc` when depending on OTP 23 or higher,
  otherwise use current implementation
  [#91](https://github.com/cabol/nebulex/issues/91)

**Fixed bugs:**

- Fixed stats to update evictions when a new generation is created and the
  older is deleted [#98](https://github.com/cabol/nebulex/issues/98)

**Closed issues:**

- Is there a way to disable caching entirely?
  [#87](https://github.com/cabol/nebulex/issues/87)
- Slow cache under moderate simultaneous load
  [#80](https://github.com/cabol/nebulex/issues/80)
- `mix nebulex.gen.cache` replaces everything in folder
  [#75](https://github.com/cabol/nebulex/issues/75)
- Replicated hash_slots for partitioned adapter
  [#65](https://github.com/cabol/nebulex/issues/65)

**Merged pull requests:**

- Overall fixes and enhancements for adapter behaviours
  [#94](https://github.com/cabol/nebulex/pull/94)
  ([cabol](https://github.com/cabol))
- Typo in code example 👀
  [#89](https://github.com/cabol/nebulex/pull/89)
  ([Awlexus](https://github.com/Awlexus))

## [v2.0.0-rc.1](https://github.com/cabol/nebulex/tree/v2.0.0-rc.1) (2020-11-15)

[Full Changelog](https://github.com/cabol/nebulex/compare/v2.0.0-rc.0...v2.0.0-rc.1)

**Implemented enhancements:**

- Made the local adapter completely agnostic to the cache name
- Added documentation in local adapter for eviction settings, caveats and
  recommendations.
- Added support for new `:pg` module since OTP 23
  [#84](https://github.com/cabol/nebulex/issues/84)

**Closed issues:**

- Error on `cache.import` using ReplicatedCache [#86](https://github.com/cabol/nebulex/issues/86)
- `{:EXIT, #PID<0.2945.0>, :normal}` [#79](https://github.com/cabol/nebulex/issues/79)
- `opts[:stats]` not getting through to the adapter [#78](https://github.com/cabol/nebulex/issues/78)
- Partitioned Cache + stats + multiple nodes causes failure [#77](https://github.com/cabol/nebulex/issues/77)
- Recommended gc settings? [#76](https://github.com/cabol/nebulex/issues/76)

**Merged pull requests:**

- Add test for unflushed messages with exits trapped [#85](https://github.com/cabol/nebulex/pull/85)
  ([garthk](https://github.com/garthk))
- Misc doc changes [#83](https://github.com/cabol/nebulex/pull/83)
  ([kianmeng](https://github.com/kianmeng))
- Use TIDs for the generation tables instead of names [#82](https://github.com/cabol/nebulex/pull/82)
  ([cabol](https://github.com/cabol))
- Update `:shards` dependency to the latest version [#81](https://github.com/cabol/nebulex/pull/81)
  ([cabol](https://github.com/cabol))

## [v2.0.0-rc.0](https://github.com/cabol/nebulex/tree/v2.0.0-rc.0) (2020-07-05)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.2.2...v2.0.0-rc.0)

**Closed issues:**

- Asynchronous testing struggles [#72](https://github.com/cabol/nebulex/issues/72)
- `MyCache.ttl/0` is undefined or private [#71](https://github.com/cabol/nebulex/issues/71)
- Add telemetry integration [#62](https://github.com/cabol/nebulex/issues/62)

**Merged pull requests:**

- Crafting Nebulex v2 [#68](https://github.com/cabol/nebulex/pull/68)
  ([cabol](https://github.com/cabol))

## [v1.2.2](https://github.com/cabol/nebulex/tree/v1.2.2) (2020-06-11)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.2.1...v1.2.2)

**Closed issues:**

- Fix: Dialyzer [#74](https://github.com/cabol/nebulex/issues/74)
- Question: Use environment variables for config [#70](https://github.com/cabol/nebulex/issues/70)

**Merged pull requests:**

- Fix: Dialyzer useless control flow [#73](https://github.com/cabol/nebulex/pull/73)
  ([filipeherculano](https://github.com/filipeherculano))

## [v1.2.1](https://github.com/cabol/nebulex/tree/v1.2.1) (2020-04-12)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.2.0...v1.2.1)

**Fixed bugs:**

- Fix issue when memory check is ran for the generation manager
  [#69](https://github.com/cabol/nebulex/issues/69)

## [v1.2.0](https://github.com/cabol/nebulex/tree/v1.2.0) (2020-03-30)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.1.1...v1.2.0)

**Implemented enhancements:**

- Refactor `Nebulex.Caching` in order to use annotated functions via decorators
  [#66](https://github.com/cabol/nebulex/issues/66)

**Fixed bugs:**

- Sporadic `:badarg` error [#52](https://github.com/cabol/nebulex/issues/52)

**Closed issues:**

- Question: disabling cache conditionally in defcacheable [#63](https://github.com/cabol/nebulex/issues/63)
- Support for persistence operations [#61](https://github.com/cabol/nebulex/issues/61)
- Implement adapter for replicated topology [#60](https://github.com/cabol/nebulex/issues/60)

**Merged pull requests:**

- [#66] Refactor `Nebulex.Caching` to use annotated functions via decorators
  [#67](https://github.com/cabol/nebulex/pull/67) ([cabol](https://github.com/cabol))
- Fixes and enhancements for `v1.2.0` [#64](https://github.com/cabol/nebulex/pull/64)
  ([cabol](https://github.com/cabol))
- Features for next release (`v1.2.0`) [#59](https://github.com/cabol/nebulex/pull/59)
  ([cabol](https://github.com/cabol))

## [v1.1.1](https://github.com/cabol/nebulex/tree/v1.1.1) (2019-11-11)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.1.0...v1.1.1)

**Implemented enhancements:**

- Add capability to limit cache size  [#53](https://github.com/cabol/nebulex/issues/53)
- Ability to "get or set" a key [#49](https://github.com/cabol/nebulex/issues/49)
- Multilevel Cache: transaction/3 is attempting to change all levels multiple times.
  [#35](https://github.com/cabol/nebulex/issues/35)

**Closed issues:**

- Pre Expire Hook [#57](https://github.com/cabol/nebulex/issues/57)
- Add matching option on returned result to Nebulex.Caching [#55](https://github.com/cabol/nebulex/issues/55)
- Multi Level with dist not working as expected [#54](https://github.com/cabol/nebulex/issues/54)
- Adapter for FoundationDB [#51](https://github.com/cabol/nebulex/issues/51)

**Merged pull requests:**

- Add match option to Nebulex.Caching [#56](https://github.com/cabol/nebulex/pull/56)
  ([polmiro](https://github.com/polmiro))

## [v1.1.0](https://github.com/cabol/nebulex/tree/v1.1.0) (2019-05-11)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.0.1...v1.1.0)

**Implemented enhancements:**

- Refactor flush action in the local adapter to delete all objects instead of
  deleting all generation tables [#48](https://github.com/cabol/nebulex/issues/48)
- Write a guide for `Nebulex.Caching` [#45](https://github.com/cabol/nebulex/issues/45)
- Turn `Nebulex.Adapter.NodeSelector` into a generic hash behavior `Nebulex.Adapter.Hash`
  [#44](https://github.com/cabol/nebulex/issues/44)
- Turn `Nebulex.Adapters.Dist.RPC` into a reusable utility [#43](https://github.com/cabol/nebulex/issues/43)
- Add support to evict multiple keys from cache in `defevict`  [#42](https://github.com/cabol/nebulex/issues/42)

**Fixed bugs:**

- custom ttl on mulltilevel cache gets overwritten [#46](https://github.com/cabol/nebulex/issues/46)

**Closed issues:**

- Will nebulex support replicating cache partitions? [#47](https://github.com/cabol/nebulex/issues/47)
- Add support to define `:opts` in `defcacheable` and `defupdatable` [#40](https://github.com/cabol/nebulex/issues/40)
- Random test failure - UndefinedFunctionError [#28](https://github.com/cabol/nebulex/issues/28)
- Adapter for Memcached [#22](https://github.com/cabol/nebulex/issues/22)
- Invalidate keys cluster-wide [#18](https://github.com/cabol/nebulex/issues/18)

**Merged pull requests:**

- Fix error when running in a release [#41](https://github.com/cabol/nebulex/pull/41)
  ([peburrows](https://github.com/peburrows))

## [v1.0.1](https://github.com/cabol/nebulex/tree/v1.0.1) (2019-01-11)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.0.0...v1.0.1)

**Fixed bugs:**

- The `:infinity` atom is being set for unexpired object when is retrieved from
  an older generation [#37](https://github.com/cabol/nebulex/issues/37)

**Closed issues:**

- Caching utility macros: `defcacheable`, `defevict` and `defupdatable`
  [#39](https://github.com/cabol/nebulex/issues/39)
- Multilevel Cache: `replicate/2` is attempting to subtract from `:infinity`
  [#34](https://github.com/cabol/nebulex/issues/34)
- `has_key?/1` does not respect ttl [#33](https://github.com/cabol/nebulex/issues/33)
- Add dialyzer and credo checks to the CI pipeline [#31](https://github.com/cabol/nebulex/issues/31)
- Fix documentation about hooks [#30](https://github.com/cabol/nebulex/issues/30)
- FAQ list [#25](https://github.com/cabol/nebulex/issues/25)

**Merged pull requests:**

- typo in transaction docs [#38](https://github.com/cabol/nebulex/pull/38)
  ([fredr](https://github.com/fredr))
- Handle an :infinity expiration in multilevel replication.
  [#36](https://github.com/cabol/nebulex/pull/36) ([sdost](https://github.com/sdost))
- Add missing coma in conf section of readme file
  [#32](https://github.com/cabol/nebulex/pull/32) ([Kociamber](https://github.com/Kociamber))

## [v1.0.0](https://github.com/cabol/nebulex/tree/v1.0.0) (2018-10-31)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.0.0-rc.3...v1.0.0)

**Implemented enhancements:**

- Refactor `Nebulex.Adapters.Dist` to use `Task` instead of `:rpc` [#24](https://github.com/cabol/nebulex/issues/24)
- Create first cache generation by default when the cache is started [#21](https://github.com/cabol/nebulex/issues/21)

**Closed issues:**

- Performance Problem. [#27](https://github.com/cabol/nebulex/issues/27)
- Cache Failing to Start on Production [#26](https://github.com/cabol/nebulex/issues/26)
- Adapter for Redis [#23](https://github.com/cabol/nebulex/issues/23)
- For `update` and `get_and_update` functions, the :ttl is being overridden
  [#19](https://github.com/cabol/nebulex/issues/19)
- TTL and EXPIRE functions? [#17](https://github.com/cabol/nebulex/issues/17)
- Publish a rc.3 release [#16](https://github.com/cabol/nebulex/issues/16)
- Replicated cache adapter [#15](https://github.com/cabol/nebulex/issues/15)
- Fulfil the open-source checklist [#1](https://github.com/cabol/nebulex/issues/1)

## [v1.0.0-rc.3](https://github.com/cabol/nebulex/tree/v1.0.0-rc.3) (2018-01-10)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.0.0-rc.2...v1.0.0-rc.3)

**Closed issues:**

- Add stream [#10](https://github.com/cabol/nebulex/issues/10)

## [v1.0.0-rc.2](https://github.com/cabol/nebulex/tree/v1.0.0-rc.2) (2017-11-25)

[Full Changelog](https://github.com/cabol/nebulex/compare/v1.0.0-rc.1...v1.0.0-rc.2)

**Closed issues:**

- Atom exhaustion from generations [#8](https://github.com/cabol/nebulex/issues/8)
- Custom ttl for every cache record? [#7](https://github.com/cabol/nebulex/issues/7)
- Load/Stress Tests [#6](https://github.com/cabol/nebulex/issues/6)
- Update Getting Started guide [#4](https://github.com/cabol/nebulex/issues/4)
- Add counters support – increments and decrements by a given amount
  [#3](https://github.com/cabol/nebulex/issues/3)

## [v1.0.0-rc.1](https://github.com/cabol/nebulex/tree/v1.0.0-rc.1) (2017-07-30)

[Full Changelog](https://github.com/cabol/nebulex/compare/64dbc38a7e330bb15a1f7372c6d3a97b82d61cc4...v1.0.0-rc.1)

**Closed issues:**

- Implement mix task to automate cache generation [#2](https://github.com/cabol/nebulex/issues/2)



\* *This Changelog was automatically generated by [github_changelog_generator](https://github.com/github-changelog-generator/github-changelog-generator)*

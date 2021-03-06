# MaidSafe Utilities - Change Log

## [0.10.0]
- Removed deprecated type and macros.
- Removed upper limit from serialisation helpers.
- Fixed log formatting regression.

## [0.9.0]
- Use config_file_handler crate to derive file locations.
- Integration with current log4rs (0.4.8) leading to changes in the log.toml specification.

## [0.8.0]
- Revert use of `unwrap!` inside `thread!`.

## [0.7.1]
- Replaced `thread!` macro with `named()` function.
- Renamed `RaiiThreadJoiner` to `Joiner`.
- Modified `SeededRng::from_seed()` to panic rather than return an error.

## [0.7.0]
- Fixed Clippy warnings.
- Added `SeededRng` type.

## [0.6.0]
- Added endian-agnostic Sip hash function.
- Added test for log.toml file.
- Replaced usage of `time` crate with `std::time`.

## [0.5.4]
- Read the config file from the binary directory instead of the current one.
- Websocket logging to the web-server writes the complete and verbose JSON when
  no pattern is specified in `log.toml` for async_web_socket.

## [0.5.3]
- Logging of date and time to web-server is now an ISO format with time-zone offset
- Unique id in log messages is string instead of u64 in JSON as 64 bit numbers are not supported out of the box in NodeJS web-servers.

## [0.5.2]
- Added ability to serialise and deserialise without being limited by the default size limit
- Websocket logging now logs unique ids as well

## [0.5.1]
- Fixed serialisation issue.
- Fixed bug in logging.
- Updated logging docs.
- Updated Contributor Agreement to version 1.1.

## [0.5.0]
- Async Logging introduced - uses log4rs.

## [0.4.1]
- Use bincode serialisation size limits.

## [0.4.0]
- Changed from using CBOR to Bincode.
- Disabled Clippy warning.

## [0.3.0]
- Added new function to allow logging to file.

## [0.2.1]
- Used quick-error for SerialisationError.

## [0.2.0]
- Clippy fixes including renaming some public enum variants.
- Formatting and style fixes.
- Limited length of filename in log output.

## [0.1.5]
- to_string() -> to_owned()
- str + str -> str.push(str)

## [0.1.4]
- Added serialisation module to encode and decode types using Cbor.

## [0.1.3]
- Added MaidSafeObserver to facilitate Routing to work with multiple event-subsets in a single thread.

## [0.1.2]
- Added env_logger initialiser.

## [0.1.1]
- Remove wildcard dependencies.

## [0.1.0]
- Thread spawning
- Thread joining via RAII
- Unwrap helpers for `Option` and `Result`
- `EventSender` for event sub-setting

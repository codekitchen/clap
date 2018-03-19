# Highlights

* Lazy propagation
* Lazy requirement validation
* `App::write_help` takes `&mut self` now
* `App::override_usage` No longer implies `\t` which allows multi lined usages
* In usage parser, for options `[name]... --option [val]` results in `ArgSettings::MultipleOccurrences` but `--option [val]...` results in `ArgSettings::MultipleValues` *and* `ArgSettings::MultipleOccurrences`. Before both resulted in the same thing
* Allow empty values no longer default
* UseValueDelimiter no longer the default
* Multpiple delima fixed (vals vs occurrences)

# Deprecations

## Simple Renames

- `App::usage` -> `App::override_usage` 
- `App::help` -> `App::override_help`
- `App::template` -> `App::help_template`
- `App::get_matches_safe` -> `App::try_get_matches` 
- `App::get_matches_from_safe` -> `App::try_get_matches_from` 
- `App::get_matches_safe_borrow` -> `App::try_get_matches_from_mut` 
- `Arg::unset` -> `Arg::unset_setting` 
- `Arg::set` -> `Arg::setting` 


## App Methods


- `App::version_message` -> `App::mut_arg`
- `App::version_short` -> `App::mut_arg`
- `App::help_message` -> `App::mut_arg`
- `App::help_short` -> `App::mut_arg`
- `App::args_from_usage` -> `App::args(&str)`
- `App::arg_from_usage` -> `App::arg(Arg::from)`
- `App::write_help` -> `&self` -> `&mut self` (#808)
- `App::gen_completions` -> `clap_completions::generate`
- `App::gen_completions_to` -> `clap_completions::generate_to`
- `Arg::from_usage` -> `Arg::from(&str)` 

# Additions

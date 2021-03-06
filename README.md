Tzdata
======

[![Build
Status](https://travis-ci.org/lau/tzdata.svg?branch=master)](https://travis-ci.org/lau/tzdata)

Tzdata. The [timezone database](https://www.iana.org/time-zones) in Elixir.

Extracted from the [Kalends](https://github.com/lau/kalends) library.

As of version 0.1.5 the tz release 2015d (from 2015-04-24 08:09:46 -0700)
is used. The tz release version can be verified with the following function:

```elixir
iex> Tzdata.tzdata_version
"2015d"
```

## Getting started

Use through the [Kalends](https://github.com/lau/kalends) library
or directly: it is available on hex as `tzdata`.

```elixir
defp deps do
  [  {:tzdata, "~> 0.1.5"},  ]
end
```

## Documentation

Documentation can be found at http://hexdocs.pm/tzdata/

## When new timezone data is released

IANA releases new versions of the [timezone database](https://www.iana.org/time-zones) frequently. When that
happens, hopefully this library will be updated within 24 hours with the new
data and a new version of the tzdata Elixir package will be released.

As an alternative to getting a new version of tzdata, users of this library
can simply run the `dl_latest_data.sh` script and then recompile tzdata. Running
that script will update the data in the `source_data` directory. The files in the
`source_data` directory contains all the information about the timezones
and is used by the tzdata library at compile time.

## License

The tzdata Elixir library is released under the MIT license. See the LICENSE file.

The tz database files (found in the source_data directory) is public domain.

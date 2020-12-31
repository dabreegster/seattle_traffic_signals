# Seattle traffic signal data

**NOTICE**: This repository is archived, and the effort to manually survey
around Seattle is on hold (it never really gained traction). The JSON data and
schema are now maintained as part of [A/B
Street](https://github.com/dabreegster/abstreet).

This is a project to map Seattle's traffic signals in detail. See [this
doc](https://docs.google.com/document/d/1Od_7WvBVYsvpY4etRI0sKmYmZnwXMAXcJxVmm8Iwdcg/edit?usp=sharing).

## Contributing

By submitting data, you agree to release your observations publicly under the
OpenStreetMap license. If you include your name in the notes, this will be
public. Feel free to remain anonymous.

## License

The license is [ODbL](https://www.openstreetmap.org/copyright), the same as
OpenStreetMap. There's no guarantee data here is correct; use it appropriately.

## Notes

Schema change to add a new field:

```shell
for x in data/*; do cat $x | jq '. + {offset_seconds: 0}' > tmp; mv -f tmp $x; done
```

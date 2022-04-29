# spatial-image-multiscale

[![Test](https://github.com/spatial-image/spatial-image-multiscale/actions/workflows/test.yml/badge.svg)](https://github.com/spatial-image/spatial-image-multiscale/actions/workflows/test.yml)

Generate a multiscale [spatial-image].

## Development

Contributions are welcome and appreciated.

To run the test suite:

```
git clone https://github.com/spatial-image/spatial-image-multiscale
cd spatial-image-multiscale
pip install -e '.[test]'
cid=$(grep 'IPFS_CID =' test/test_spatial_image_multiscale.py | cut -d ' ' -f 3 | tr -d '"')
# Needs ipfs, e.g. https://docs.ipfs.io/install/ipfs-desktop/
ipfs get -o ./test/data -- $cid
pytest
```

[spatial-image]: https://github.com/spatial-image/spatial-image
[Xarray]: https://xarray.pydata.org/en/stable/

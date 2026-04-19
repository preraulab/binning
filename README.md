# binning

Bin values or events onto regular grids, in 1-D or N-D, with fixed edges or a sliding window.

Part of the Prerau Lab [`utils`](https://github.com/preraulab/utils) meta-repository. Can also be used standalone.

## When to use which

| Need | Use |
|---|---|
| Count values in fixed 1-D bins | `create_bins` |
| Count values on a multi-dimensional grid | `create_NDbins` |
| Count in overlapping windows (non-disjoint bins) | `hist_slide` |

## Functions

### `create_bins`

Create 1-D bins with optional overlap.

```matlab
[bin_edges, bin_centers] = create_bins(bin_range, bin_width, bin_step, bin_method)
```

### `create_NDbins`

Create N-dimensional bins with optional overlap. Same parameters as `create_bins` but accepts vectors of ranges/widths/steps (one per dimension).

### `hist_slide`

Create an N-dimensional histogram with sliding (optionally overlapping) bins.

```matlab
[counts, bin_centers] = hist_slide(data, 'Name', Value, ...)
```

See `help <function>` at the MATLAB prompt for the full docstring of each.

## Install

```matlab
addpath('/path/to/binning');
```

When used as part of a larger toolbox (e.g. `utils`), the top-level path setup handles this automatically.

## Dependencies

MATLAB R2020a+. No required toolboxes.

## License

BSD 3-Clause. See [`LICENSE`](LICENSE).

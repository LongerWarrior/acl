# Compressing scalar tracks

Once you have created a [raw track list](creating_a_raw_track_list.md) and an [allocator instance](implementing_an_allocator.md), you are ready to compress it.

For now, we only implement a single algorithm: [uniformly sampled](algorithm_uniformly_sampled.md). This is a simple and excellent algorithm to use for everyday animation clips. Segmenting is currently not supported.

Compression settings are currently required as an argument but not used. It is a placeholder.

```c++
#include <acl1_3/compression/compress.h>

using namespace acl1_3;

compression_settings settings;

OutputStats stats;
compressed_tracks* out_compressed_tracks = nullptr;
ErrorResult error_result = compress_track_list(allocator, raw_track_list, settings, out_compressed_tracks, stats);
```

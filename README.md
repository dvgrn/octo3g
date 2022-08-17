This repo is intended as a replacement for the glider-collisions repo at

  https://github.com/dvgrn/glider-collisions

Instead of population-based hashes, it uses the get-octohash() function in

  https://github.com/dvgrn/octohash

to record a searchable 9-byte orientation-independent hash for each stage of every three-glider collision.

This means that an octo3g search can accurately find both active reactions and settled constellations, using the same search script, with few or no false positives.

Limitations
-----------
Something that has not yet been done is to reprocess the full list of 3-glider collisions, to put them all in Shinjuku format for example, or otherwise filter out the duplicates.  There are currently quite a few duplicated reactions where the same essential collision is recorded in different orientations, or rewound different numbers of ticks from the first collision point.

Given that known limitation, synthesise-patt.py has no advantages over find-octo3g.py (searching for three-glider active reactions).  synth-const-4G-Python3.py has two possible advantages: find-octo3g.py may report a few more duplicates, and it won't report any 4G collision results (until hash files are added for the final ash outputs of all the 4G collisions searched by synth-const-4G-Python3.py -- but that should be a fairly easy addition.)

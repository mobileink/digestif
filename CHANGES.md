v0.7.1 2018-11-15 Paris (France)
--------------------------------

- Cross compilation adjustments (@hannesm) (# 76)
- Add the WHIRLPOOL hash algorithm (@clecat) (#77)
- Backport fix on opam file (@dinosaure, @kit-ty-kate)

v0.7 2018-10-15 Paris (France)
--------------------------------

- Fixed HMAC on BLAKE2{S,B} (@emillon) (#46, #51)
- Fixed `convenient_of_hex` (@dinosaure, @hannesm, @cfcs) (#55)
- Add `of_raw_string`/`to_raw_string` (@samoht) (#57)
- Test `digestif` on solo5 and xen backends (@samoht)
- *breaking change*, commont type `t` is an abstract type (#58, #56)
- Fixed META file (@dinosaure, @g2p) (#75)
- New dependency `eqaf` (@dinosaure, @cfcs, @hannesm) (constant-time equal function) (#33, #34, #48, #50, #52, #65)
- Remove `Obj.magic` in common implementation (@dinosaure, @samoht) (#61, #62)
- Add conveniences functions in common implementation (@hcarty) (#63)
- Add option-returning functions in common implementation (@harcty) (#63)
- Verify length of string on `of_raw_string` function (@hcarty) (#63)
- Release runtime lock (@andersfugmann, @dinosaure, @cfcs) (#69, #70)
- Bounds check (@cfcs, @dinosaure) (#71, #72)
- Fixed linking problem (@andersfugmann, @g2p, @dinosaure) (#49, #53, #73, #74)
- Update OPAM file (@dinosaure)

v0.6.1 2018-07-24 Paris (France)
--------------------------------

- *breaking change* API: Digestif implements a true linking trick. End-user need
  to explicitely link with `digestif.{c,ocaml}` and it needs to be the first of
  your dependencies.
- move to `jbuilder`/`dune`

v0.6 2018-07-05 Paris (France)
------------------------------

- *breaking change* API:
  From a consensus between people who use `digestif`, we decide to delete `*.Bytes.*` and `*.Bigstring.*` sub-modules.
  We replace it by `feed_{bytes,string,bigstring}` (`digest_`, and `hmac_` too)
- *breaking change* semantic: streaming and referentially transparent
  Add `feedi_{bytes,string,bigstring}`, `digesti_{bytes,string,bigstring}` and `hmaci_{bytes,string,bigstring}`
  (@hannesm, @cfcs)
- Constant time for `eq`/`neq` functions
  (@cfcs)
- *breaking change* semantic on `compare` and `unsafe_compare`:
  `compare` is not a lexicographical comparison function (rename to `unsafe_compare`)
  (@cfcs)
- Add `consistent_of_hex` (@hannesm, @cfcs)

v0.4 2017-10-30 Mysore / ಮೈಸೂರು (India)
----------------------------------------

- Add an automatised test suit
- Add the RIPEMD160 hash algorithm
- Add the BLAKE2S hash algorithm
- Update authors
- Add `feed_bytes` and `feed_bigstring` for `Bytes` and `Bigstring`

v0.3 2017-07-21 Phnom Penh (Cambodia)
-------------------------------------

- Fixed issue #6
- Make a new test suit

v0.2 2017-07-05 Phnom Penh (Cambodia)
-------------------------------------

- Implementation of the hash function in pure OCaml
- Link improvement (à la `mtime`) to decide to use the C stub or the OCaml implementation
- Improvement of the common interface (pretty-print, type t, etc.)

v0.1 2017-05-12 Rạch Giá (Vietnam)
------------------------------------

- First release

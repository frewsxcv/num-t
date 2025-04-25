# num-t

`Num<T>`: Associate arbitrary types with numeric types

This crate provides the `Num<Number, Type>` struct, which allows you to associate an arbitrary type `Type` with a numeric value `Number`. This can be useful for creating strongly-typed numeric values, preventing mixing of different units or concepts in calculations.

`Num<Number, Type>` wraps a numeric type `Number` and uses a `std::marker::PhantomData<Type>` to carry the type information without adding runtime overhead.

It implements many standard traits, including:

- `Clone`, `Copy`, `Default`
- `From<Scalar>`
- `PartialOrd`, `PartialEq`, `Eq`
- Arithmetic operators (`Add`, `Sub`, `Mul`, `Div`, `Rem`, `AddAssign`, etc.)
- `FromStr`, `Display`
- `Sum`
- Traits from the `num-traits` crate: `ToPrimitive`, `NumCast`, `Num`, `One`, `Zero`, `Float`, `Bounded`, `Signed`, `FromPrimitive`.

## Optional Features

- `float_next_after`: Implements `float_next_after::NextAfter` for `Num` when the underlying `Number` type also implements it.
- `geo`: Implements `geo::GeoNum` for `Num` when the underlying `Number` type also implements it.

## License

This crate is licensed under either of

* Apache License, Version 2.0
* MIT license

at your option.

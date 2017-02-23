We spent quite a while talking about whether a monoid M (thought of as a one object category) could be *equivalent* to its opposite.

First, I want to point out that this is not what Leinster was actually asking in 1.2.23(b) --- he asked if it could be *isomorphic* to its opposite, contrary to my insistence that you shouldn't even talk about isomorphism of categories, only equivalence.

**Lemma.** A _functor_ between monoids is exactly a monoid homomorphism.
**Lemma.** A _natural transformation_ between two monoid homomorphisms `F,G : M → N` is an element `s : N` showing that `F` and `G` are conjugate,
i.e. `s G(r) = F(r) s` for all `r : M`.
**Lemma.** A natural transformation is a _natural isomorphism_ if the element `s : N` is invertible.

(These are all straightforward exercises.)

Thus an _equivalence_ between monoids `M, N` consists of a pair of monoid homomorphisms `F : M → N` and `G : N → M`, and invertible elements `m : M`, `n : N`, such that `m F(G(r)) = r m` for all `r : M`, and `n G(F(s)) = s n` for all `s : N`. It is an isomorphism only if `m` and `n` are the identities.

Let's first try to find a monoid `M` not _isomorphic_ to its opposite.
* The free monoid we discussed in class was not useful --- the map which reverses words is a perfectly good functor.
* No commutative monoid can work, since then the identity map will be a functor, and easily enough an isomorphism.
* There are [two good solutions](http://math.stackexchange.com/questions/484102/is-every-monoid-isomorphic-to-its-opposite) on Stack Exchange:
    * `End(X)` for any set `X` with at least two elements, because any constant function is left-absorbing (i.e. `c ∘ f = c` for any `f : End(X)`), but there are no right-absorbing functions, and an anti-isomorphism `End(X) → End(X)` would have to take left-absorbing elements to right-absorbing elements.
    * The monoid with elements `{ 1, a, b }` satisfying `a a = a`, `a b = a`, `b a = b`, `b b = b` easily gives another counterexample.

Are these counterexamples also not _equivalent_ to their opposites?
* The second example is easy: the only invertible element is `1`, so equivalence immediately reduces to isomorphism. (That is, this monoid is not even equivalent to its opposite.)
* The endomorphism example is a bit trickier... using the characterisation of equivalences as functors which are fully faithful and essentially surjective, we can see that the homomorphism `F` must be a bijection, and from this we can see that the image of a left-absorbing elements must be right-absorbing, giving the same contradiction as above. Is there an easier way, that doesn't go via that characterisation?
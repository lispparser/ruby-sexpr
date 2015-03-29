Ruby SExpr
==========

SExpr is a library for parsing a subset of s-expressions, namely cons
aren't handled and replaced by more convenient lists. So something
like:

    (foo (bar baz))

is parsed properly, but something like:

    (foo . ((bar . (baz . ())) . ()))

isn't handled and gives a syntax error, even so they would be
equivalent in a full SExpr style parser.

SExpr isn't meant to be fast, but meant to be as verbose as possible,
meaning it can give you the line and column of a given SExpr and parse
comments and whitespace as well if required.

Beside the basic parser SExpr also contains a xschema-like verifier in
the form of SExpr::Schema and a simple helper in the form of
SExpr::Reader that gives XPath like features.


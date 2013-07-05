For the most part, NodeBB follows the [Google Javascript Style Guide](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

## Code Formatting

**Please Note**: The existing codebase as of July 2013 does not adhere to this style guide 100%. If you see instances where the style guide is not adhered to, feel free to restyle and send off a pull request.

### Indentation & Bracing

NodeBB uses tabbed indentation. Bracing should follow the [One True Brace Style](http://en.wikipedia.org/wiki/Indent_style#Variant:_1TBS):

    if (condition) {
        // code here ...
    } else {
        // otherwise ...
    }

Put conditionals and statements on separate lines :

    if (leTired) 
        haveANap();

### Variables

Variables should always be prefaced with the `var` keyword

    var foo = 'bar';

Multiple declarations are to be included in the same `var` statement:

    var foo = 'bar',
        bar = 'baz';

### Semicolons

Use semicolons if at all possible

## Naming

CamelCase if at all possible:

> functionNamesLikeThis, variableNamesLikeThis, ClassNamesLikeThis, EnumNamesLikeThis, methodNamesLikeThis, CONSTANT_VALUES_LIKE_THIS, foo.namespaceNamesLikeThis.bar, and filenameslikethis.js.
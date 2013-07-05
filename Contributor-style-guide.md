## Code Formatting

### Indentation & Bracing

NodeBB uses tabbed indentation. Bracing should follow the [One True Brace Style](http://en.wikipedia.org/wiki/Indent_style#Variant:_1TBS):

    if (condition) {
        // code here ...
    } else {
        // otherwise ...
    }

### Variables

Local variables should always be prefaced with the `var` keyword

    var foo = 'bar';

Multiple declarations are to be included in the same `var` statement:

    var foo = 'bar',
        bar = 'baz';
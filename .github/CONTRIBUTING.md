## Issues

Before posting an Issue, please do a quick search in Issues to see if a similar Issue is already created. If the documentation has a FAQ (Frequently Asked Questions), please also check out the entries there.

## Pull Requests

- Committed files in PRs must follow one of these two coding styles:

**A. New (Preferred)**

This is basically the universal C# coding style. My plugins will gradually switch over to this style (I'll commit the modified lines in this style). Use spaces instead of tabs.

```csharp
for (int i = 0; i < array.Length; i++)
{
    int value = array[i];
    if (value < 0)
        continue;

    Debug.Log("Value ASCII " + (char)value);
}
```

**B. Old**

The style that is used in almost every part of my plugins. [Use tabs instead of spaces](https://www.youtube.com/watch?v=SsoOG6ZeyUI).

```csharp
for( int i = 0; i < array.Length; i++ )
{
	int value = array[i];
	if( value < 0 )
		continue;

	Debug.Log( "Value ASCII " + (char) value );
}
```

- Ensure that there are no changes in lines that you haven't touched!
- For consistency, you must use *Windows CRLF* line endings (can be changed from the bottom right corner in Visual Studio, see the yellow arrow below)

![Line Endings](Images/VSLineEndings.png)

- You mustn't use LINQ. If I see potential optimization issues in the code, I may ask you to refactor those parts
- Don't use the `var` keyword. I want variables types to be declared explicitly. But while calling constructors, you can use the shorthand `new(...)` format


## Snippet 1 Test

To test snippet 1 I implemented the following code:

```
@Test
    public void testSnip1() throws IOException{
        Path fileName = Path.of("snip1.md");
        // Path fileName = Path.of("snippet1.md");
        String content = Files.readString(fileName);
        List<String> links = MarkdownParse.getLinks(content);
        List<String> expected = List.of("url.com, `google.com", "google.com", "ucsd.edu");

        assertEquals(expected, links);
    }
```

This was the output of my implenation for snippet 1:
![Image](mysnippet1.png)

This was the output of week 7's implementation for snippet 1:
![Image](7snippet1.png)

## Snippet 2 Test

To test snippet 2 I implemented the following code:

```
@Test
    public void testSnip1() throws IOException{
        Path fileName = Path.of("snip1.md");
        // Path fileName = Path.of("snippet1.md");
        String content = Files.readString(fileName);
        List<String> links = MarkdownParse.getLinks(content);
        List<String> expected = List.of("url.com, `google.com", "google.com", "ucsd.edu");

        assertEquals(expected, links);
    }
```

This was the output of my implenation for snippet 2:
![Image](mysnippet2.png)

This was the output of week 7's implementation for snippet 2:
![Image](7snippet2.png)

## Snippet 3 Test

To test snippet 3 I implemented the following code:

```
@Test
    public void testSnip1() throws IOException{
        Path fileName = Path.of("snip1.md");
        // Path fileName = Path.of("snippet1.md");
        String content = Files.readString(fileName);
        List<String> links = MarkdownParse.getLinks(content);
        List<String> expected = List.of("url.com, `google.com", "google.com", "ucsd.edu");

        assertEquals(expected, links);
    }
```

This was the output of my implenation for snippet 3:
![Image](mysnippet3.png)

This was the output of week 7's implementation for snippet 3:
![Image](7snippet3.png)




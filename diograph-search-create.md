# Diograph Search Create

Combined input field for searching and creating diories.
It suggests diories as search results or diories to be created.

```
<DiographSearchCreate onFocusClick={(diory) => { this.setState({inFocus: diory}) }} />
```

**onFocusClick** property takes a function.
- onFocusClick function is triggered every time a search result is clicked
- clicked diory object is given as an argument to onFocusClick function


# VS Code Go Snippets
-------------------

This extension contains code snippets for Go syntax for [Vs Code][code] editor.


## Installation

In order to install an extension you need to launch the Command Palette (Ctrl + Shift + P or Cmd + Shift + P) and type Extensions.
There you have either the option to show the already installed snippets or install new ones. Search for *honnamkuan.go-snippets* and install it.

## Supported languages (file extensions)
* Go (.go)

## Snippets

Below is a list of all available snippets and the triggers of each one.

### General
| Trigger  | Content |
| -------: | ------- |
| `vv`   | initialize variable `varName := value`|
| `ier`   | if error `if err != nil { myStatements }` |
| `ifok`   | if ok `if value,ok := myFunc; ok { myStatements } `|
| `fr`   | for range `for _, v := range values { myStatements }`|
| `frr`   | for range channel `for v := range channel { myStatements }`|
| `def`   | case default `default:` |
| `cl`   | close `close(closable)` |
| `fms`   | fmt Sprinf `fmt.Sprintf("%+v", args)` |


### Types
| Trigger  | Content |
| -------: | ------- |
| `st`   | struct type <pre>type structName struct {<br/><br/>}</pre>|
| `sf`   | struct field `fieldName string`|
| `stt`   | struct tag `` `json:"jsonFieldName"` ``|
| `ne`   | struct constructor method <pre>func NewFoo() *Foo {<br/><br/>  return &Foo{<br/><br/>  }<br/>}</pre>|
| `inte`   | Interface type <pre>type interfaceName interface {<br/><br/>}|


### Collection manipulation
| Trigger  | Content |
| -------: | ------- |
| `sr`   | remove one element from slice `slice = append(slice[:index], slice[index+1:]...)` |
| `ap`   | append element to slice `slice = append(slice, element)` |
| `del`   | delete map element by key `delete(map, key)`|




### Return values
| Trigger  | Content |
| -------: | ------- |
| `rn`   | Return Nil `return nil`|
| `rne`   | Return Nil and err `return nil, err`|
| `re`   | Return err `return err`|


### Logging
| Trigger  | Content |
| -------: | ------- |
| `lo`   | log variable `log.Printf("%+v\n", varName)` |
| `le`   | log error `log.Printf("%+v\n", err)` |


### Error Handling
| Trigger  | Content |
| -------: | ------- |
| `es`   | errors with stack `errors.WithStack(err)`|
| `em`   | error with message `errors.WithMessage(err, message)`|
| `emf`   | error with messagef `errors.WithMessagef(err, format, args)`|
| `is`   | errors Is `if errors.Is(err, MyError) { myStatements }`|
| `as`   | errors As <pre>var e ErrorType<br/>errors<span>.</span>As(err, &e) {<br/>  myStatements<br/>}</pre> |


### Concurrency
| Trigger  | Content |
| -------: | ------- |
| `gofunc`   | anonymous go function `go func() { myStatements }` |
| `defunc`   | anonymous defer function `defer func { myStatements }`|
| `lock`   | sync.Mutex Lock and defer Unlock <pre>mu.Lock()<br/>defer mu.Unlock()</pre>|
| `nb` | non-blocking channel send <pre>select {<br/>case msg <- msgChan:<br/>default:<br/>}</pre>|


[code]: https://code.visualstudio.com/
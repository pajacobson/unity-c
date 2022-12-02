# Unity-C

Sublime Text 4 autocompletions for [Unity - Unit Testing For C (Especially Embedded Software)](http://www.throwtheswitch.org/unity).


## Unity Completions

Unity `test assert` snippets are active when the caret is positioned within a function body .

Snippets are triggered by abbreviation of the assert name.
With few exceptions the trigger is the first letter of each word in the name, ignoring the test prefix.

Abbreviations can resolve to more than one snippet.
`aem` is used for `assert_empty_message`, `assert_equal_message` and `assert_equal_memory`.
Adding extra characters to the trigger doesn't make the issue significantly better, and adds unnecessary keystrokes. Pick the desired option from the completions pop-up and move on.

#### Basic fail and ignore
| Shortcut  | Assertion |
|:--|:--|
| `pa` | `TEST_PASS` |
| `pam` | `TEST_PASS_MESSAGE` |
| `fa` | `TEST_FAIL` |
| `fam` | `TEST_FAIL_MESSAGE` |
| `ig` | `TEST_IGNORE` |
| `igm` | `TEST_IGNORE_MESSAGE` |

#### `boolean` types
| Shortcut | Assertion  |
|:--|:--|
| `at` | `TEST_ASSERT_TRUE` |
| `au` | `TEST_ASSERT_UNLESS` |
| `af` | `TEST_ASSERT_FALSE` |
| `an` | `TEST_ASSERT_NULL` |
| `ann` | `TEST_ASSERT_NOT_NULL` |
| `ae` | `TEST_ASSERT_EMPTY` |
| `ane` | `TEST_ASSERT_NOT_EMPTY` |

`
#### `integer` types
| Shortcut | Assertion |
|:--|:--|
|`aex` | `TEST_ASSERT_EQUAL_X` |
|`aeex` | `TEST_ASSERT_EACH_EQUAL_X` |
|`agtx` | `TEST_ASSERT_GREATER_THAN_X` |
|`agoex` | `TEST_ASSERT_GREATER_OR_EQUAL_X` |
|`altx` | `TEST_ASSERT_LESS_THAN_X` |
|`aloex` | `TEST_ASSERT_LESS_OR_EQUAL_X` |
|`anex` | `TEST_ASSERT_NOT_EQUAL_X` |
|`axw` | `TEST_ASSERT_X_WITHIN` |
|`aexa` | `TEST_ASSERT_EQUAL_X_ARRAY` |
|`axaw` | `TEST_ASSERT_X_ARRAY_WITHIN` |

Where `x` is:
- `i`, `i8`, `i16`, `i32`, `i64`
- `u`, `u8`, `u16`, `u32`, `u64`
- `h`, `h8`, `h16`, `h32`, `h64`
- `c`: char
- `sz`: size_t

#### `double` and `float` types
| Shortcut | Assertion |
|:--|:--|
|`axw` | `TEST_ASSERT_X_WITHIN` |
|`aex` | `TEST_ASSERT_EQUAL_X`  |
|`aexa` | `TEST_ASSERT_EQUAL_X_ARRAY` |
|`aeex` | `TEST_ASSERT_EACH_EQUAL_X` |

Where `x` is:
- `d`: double
- `f`: float


#### `struct` and `string` types
| Shortcut | Assertion |
|:--|:--|
|`aeex` | `TEST_ASSERT_EACH_EQUAL_X` |
|`aex`  | `TEST_ASSERT_EQUAL_X` |
|`aexa` | `TEST_ASSERT_EQUAL_X_ARRAY` |

Where `x` is:
- `p`: pointer
- `s`: string
- `m`: memory


### Messages
Append `m` to a trigger to access the message variant.

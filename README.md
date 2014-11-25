# picolisp-mode - major mode for PicoLisp programming

*Author:* Alexis <flexibeast@gmail.com><br>
*URL:* [https://github.com/flexibeast/picolisp-mode](https://github.com/flexibeast/picolisp-mode)<br>

`picolisp-mode` provides a major mode for PicoLisp programming.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Issues](#issues)
- [License](#license)

## Features

* Syntax highlighting of PicoLisp code. (But please read the below [note on syntax highlighting](#note).)

* Comint-based `pil` REPL buffers.

* Quick access to documentation for symbol at point.

## Installation

Install [picolisp-mode from MELPA](http://melpa.org/#/picolisp-mode), or put the `picolisp-mode` folder in your load-path and do a `(require 'picolisp-mode)'.

## Usage

Enable syntax highlighting for a PicoLisp source buffer with <kbd>M-x picolisp-mode</kbd>. 

Start a `pil` REPL session with <kbd>M-x picolisp-repl</kbd>.

Access documentation for the function at point with <kbd>C-c C-d</kbd> (`picolisp-describe-symbol`). By default, documentation will be displayed via the `lynx` HTML browser. However, one can set the value of `picolisp-documentation-method` to either a string containing the absolute path to an alternative browser, or - for users of Emacs 24.4 and above - to the symbol `'picolisp-display-documentation`; this function uses the `shr` library to display the documentation in an Emacs buffer. The absolute path to the documentation is specified via `picolisp-documentation-path`, and defaults to `/usr/share/doc/picolisp/doc/`.

The various customisation options, including the faces used for syntax highlighting, are available via the `picolisp` customize-group.

<a name="note"></a>

### A note on syntax highlighting

PicoLisp's creator is opposed to syntax highlighting of symbols in PicoLisp, for [good reasons](http://www.mail-archive.com/picolisp@software-lab.de/msg05019.html). However, some - such as the author of this package! - feel that, even taking such issues into consideration, the benefits can outweigh the costs. (For example, when learning PicoLisp, it can be useful to get immediate visual feedback about unintentionally redefining a PicoLisp 'builtin'.) To accommodate both views, syntax highlighting can be enabled or disabled via the `picolisp-syntax-highlighting-p` variable; by default, it is set to `t` (enabled).
<a name="issues"></a>

## Issues / bugs

If you discover an issue or bug in `picolisp-mode` not already noted:

* as a TODO item, or

* in [the project's "Issues" section on GitHub](https://github.com/flexibeast/picolisp-mode/issues),

please create a new issue with as much detail as possible, including:

* which version of Emacs you're running on which operating system, and

* how you installed `picolisp-mode`.

## License

[GNU General Public License version 3](http://www.gnu.org/licenses/gpl.html), or (at your option) any later version.


---
Converted from `picolisp-mode.el` by [*el2markdown*](https://github.com/Lindydancer/el2markdown).
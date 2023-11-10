[![Melpa Status](http://melpa.org/packages/nixpkgs-fmt-badge.svg)](http://melpa.org/#/nixpkgs-fmt)
[![Melpa Stable Status](http://stable.melpa.org/packages/nixpkgs-fmt-badge.svg)](http://stable.melpa.org/#/nixpkgs-fmt)
[![Build Status](https://github.com/purcell/emacs-nixpkgs-fmt/actions/workflows/test.yml/badge.svg)](https://github.com/purcell/emacs-nixpkgs-fmt/actions/workflows/test.yml)
<a href="https://www.patreon.com/sanityinc"><img alt="Support me" src="https://img.shields.io/badge/Support%20Me-%F0%9F%92%97-ff69b4.svg"></a>

nixpkgs-fmt.el
==============

This Emacs library provides commands and a minor mode for easily reformatting
Nix source code using the [nixpkgs-fmt][nixpkgs-fmt] command.

Installation
=============

If you choose not to use one of the convenient
packages in [MELPA][melpa], you'll need to
add the directory containing `nixpkgs-fmt.el` to your `load-path`, and
then `(require 'nixpkgs-fmt)`.

Usage
=====

Customise the `nixpkgs-fmt-command` variable as desired, then call
`nixpkgs-fmt-buffer` or `nixpkgs-fmt-region` as convenient.

Enable `nixpkgs-fmt-on-save-mode` in Nix buffers like this:

```el
(add-hook 'nix-mode-hook 'nixpkgs-fmt-on-save-mode)
```

or locally to your project with a form in your .dir-locals.el like
this:

```el
((nix-mode
   (mode . nixpkgs-fmt-on-save)))
```

You might like to bind `nixpkgs-fmt` or `nixpkgs-fmt-buffer` to a key,
e.g. with:

```el
(define-key 'nix-mode-map (kbd "C-c C-f") 'nixpkgs-fmt)
```

[melpa]: http://melpa.org
[nixpkgs-fmt]: https://github.com/nix-community/nixpkgs-fmt

<hr>

[💝 Support this project and my other Open Source work](https://www.patreon.com/sanityinc)

[💼 LinkedIn profile](https://uk.linkedin.com/in/stevepurcell)

[✍ sanityinc.com](http://www.sanityinc.com/)

[🐦 @sanityinc](https://twitter.com/sanityinc)

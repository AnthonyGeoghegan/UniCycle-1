=======================
UniCycle Plugin for Vim
=======================

This GitHub repository is a fork of
http://www.vim.org/scripts/script.php?script_id=1384\ .


Overview
========

This script cycles through certain Unicode characters while typing. It only
works if set encoding=utf-8.

When on, the hyphen (-), period (.), apostrophe ('), and quote (")
characters are mapped to the appropriate functions within this file.

When you enter two hyphen characters in a row, the first hyphen character
will cycle to an EN DASH character. A third hyphen will turn the EN DASH
into an EM DASH. A fourth hyphen will turn your EM DASH back into a
HYPHEN-MINUS.

Entering three periods in a row will replace all three periods with a
HORIZONTAL ELLIPSIS character.

Entering an apostrophe will try to determine if the apostrophe should be a
LEFT SINGLE QUOTATION MARK or RIGHT SINGLE QUOTATION MARK. It does this by
looking at the character to the left of the new character. You can cycle
between LEFT SINGLE QUOTATION MARK, APOSTROPHE, and RIGHT SINGLE QUOTATION
MARK by repeatedly hitting your apostrophe key.

Quote characters are treated in the same manner as apostrophe characters.
You get either a LEFT DOUBLE QUOTATION MARK, normal QUOTATION MARK, or RIGHT
DOUBLE QUOTATION MARK based on the previous character and how many times you
hit your quote key in a row.


Installation
============

Either drop into your ~/.vim/plugins/ folder, or install using your
favorite plugin manager (I recommend `Pathogen`_).


Using
=====

Execute the ``:UniCycleOn`` command to activate UniCycle in the current
buffer. To automatically activate UniCycle for a specific file type, use
an autocommand, as in::

    autocmd FileType rst UniCycleOn

You can toggle UniCycle on and off using the ``:UniCycleToggle`` command.
This is useful in maps; for instance if you put::

    nnoremap <C-u><C-u> :UniCycleToggle<cr>

In your .vimrc you can turn UniCycle on and off by pressing ``Ctrl+U``
twice.

UniCycle is buffer-local, so turning it on in one buffer will not affect
any other buffers.


Authors and License
===================

This plugin was originally written by `Jason Diamond`_. I (`Joseph Irwin`_)
have made some improvements (making functions script-local, and the
mappings buffer-local) and included some modifications from `Micah
Elliott`_.

Jason Diamond placed this plugin into the public domain; I have added
the `CC0`_ copyright waiver here to make this clearer and more effective.


License:
--------

.. image:: http://i.creativecommons.org/p/zero/1.0/88x31.png
    :alt: CC0
    :target: http://creativecommons.org/publicdomain/zero/1.0/

To the extent possible under law, the authors have waived all
copyright and related or neighboring rights to UniCycle.


.. _Pathogen: https://github.com/tpope/vim-pathogen
.. _`Jason Diamond`: http://jason.diamond.name/
.. _`Joseph Irwin`: https://github.com/cordarei/
.. _`Micah Elliott`: https://github.com/MicahElliott/
.. _CC0: http://wiki.creativecommons.org/CC0

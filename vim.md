Entering insert mode
===

    i - Enter insert mode at cursor
    I - Enter insert mode at the first non blank character
    s - Delete character under cursor and enter insert mode
    S - Delete the whole line and enter insert mode at the BOL
    a - Enter insert mode after the cursor
    A - Enter insert mode at the end of the line
    o - Enter insert mode on the next line
    O - Enter insert mode above the current line
    C - Delete from cursor to the end of the line and enter insert mode

Basics: wWbBeE

    w - Forward to the beginning of the next word
    W - Forward to the beginning of the next WORD
    b - Backward to the next beginning of a word
    B - Backward to the next beginning of a WORD
    e - Forward to the next end of a word
    E - Forward to the next end of a WORD
    0 - Move to the zeroth character of the line
    ^ - Move to the first non blank character of the line
    $ - Move to the end of the line

    note: WORD is all chars separated by withe spaces
    /home/user/folder is 6 words but juste one WORD

Slightly less basic: fFtT
Allow follow [(n)um]<verb><n(o)un> syntax

    [n]f<o> - Forward until (nth) (o)  (Inclusive)
    [n]F<o> - Backward until (nth) (o) (Inclusive)
    [n]t<o> - Forward until (nth) (o)  (Exclusive)
    [n]T<o> - Backward until (nth) (o) (Exclusive)
    
Searching
===

    /  - Forward
    ?  - Backward
    *  - Word under cursor - forward (bounded)
    g* - Word under cursor - forward (unbounded)
    #  - Word under cursor - backward (bounded)
    g# - Word under cursor - backward (unbounded)
    n  - Next result, forward
    N  - Next result, backward

Copy/Paste
===

    y - Yank. Example: yw (yank word)
    p - Paste after cursor
    P - Paste before cursor

Do/Redo
===

    u - Undo stuff
    Ctrl R - Redo stuff
    
Common edit commands
===

    d - Delete: [range]d<motion>
            dd  - delete current line
	    dj  - delete current and next line
	    2dj - delete current and 2 lines downwards

    c - Change (same as d but enter insert mode)
            cw  - change word
	    cc  - do the same as S. Delete entire line and enter insert mode
	    2dw - delete 2 words and enter insert mode

    ~  - Toogle the case of the caracter under cursor
    g~ - Toogle case of [motion]
            ex: tr|ue -> g~w -> trUE
	    ex: tr|ue -> g~iw -> TRUE

    p  - Paste	    

Registers
===
Accessing:

        "<reg> - ex: "ayy - Yank current line into 'a' register
	             "ap  - Paste 'a' register

        <C-r><reg> - Paste content of the <reg>

Linsting:
        :reg

Special registers:
        " - noname buffer - last dcsxy
	_ - black hole buffer
        % - filename
	/ - last search
	: - last command
	. - last edit

Register assignement commands
====

        y - Yank
	q - Macro
	m - Marks

Advanced motion
===

    () - Sentences (". " separated words)
    {} - Paragraphs (next empty line)
    ; - Repeat last motion forward
    , - Repeat last motion backward
    g<hjkl> - Go down a _visual_ line 
    <#>G - Go to line #
    gg - top of file
    % - matching brace/bracket/paren/tag (with machtag plugin)

Text objects
===
    
    {}[]()w<>t'"`

        i - Inside
	a - Around

Misc. commands
===

    [count](<|>) - Indent count lines
    <range>[count] (<|>) - Indent given range count times
    . - redo last change
    zz - center screen
    ZZ - Write and quit. Write only if there's changes
    :%s/foo/bar/g - Search and replace globally in all lines

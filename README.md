 <h1 class="title">CAESAR documentation</h1>
    <p><h2>What is CAESAR?</h2>
    Caesar is an <b>esolang</b>. That means that it's a programming language that is not
supposed to be used for actual, useful purpose. Sometimes, its a work of art, but sometimes,
like this time, its only purpose is to cause headache. Unlike other esolangs, though, it has
pretty readabil-ish syntax. It was made in one evening by a 15yo. who is bad at
programming language design and programming, so dont expect much.</p>
<p><h2>How does it work?</h2>
The esolang is named after the Roman general <b>Gaius Julius Caesar.</b>
Yes, you're now gonna be performing army.. more like exercise. It was loosely inspired by the Caesar
problem from children algorithmisation book.  So you essntially have 3 main subjects:
<ul>
    <li><b>Caesar/Commander</b> - a subject that performs most oerations. He prints to the output, he controls the program
    flow and he decides when we end. But he is dumb, so he  can only remember one information at one time</li>
    <li><b>Basket</b> - essntially a stack with fancy name</li>
    <li><b>Army</b> - a subject that essentially operates the stack. They can receive commands from Caesar, perform basic operations (like addition or shuffling the stack),
    can receive information from him and send him information.</li>
</ul></p>
<p><h2>Commands</h2>
This esolang contains only like 10 commands that are as following:
<ul>
    <li><span class="hl">raise x</span> - raise flags A-F</li>
    <li><span class="hl">yell</span> - prints the content of Caesar's memory to the output</li>
    <li><span class="hl">listen</span> - listens for user input, saves it to commander memory</li>
    <li><span class="hl">save</span> - saves evenrything presented as argument to the Caesar's memory</li>
    <li><span class="hl">signal</span> - pushes the value in Caesar's memory to the basket</li>
    <li><span class="hl">#</span> - comment</li>
    <li><span class="hl">if x y</span> - if the value in the Caesar's memory is equal to x, do y</li>
    <li><span class="hl">if! x y</span> - same as if but actvates if x isn't equal to memory</li>
    <li><span class="hl">move</span> - move to the beggining of the program</li>
    <li><span class="hl">stop</span> - stops the program's execution</li></ul>
    raise arguments:
    <ul><li><span class=hl>A</span> - put the value on top of the stack to the bottom</li>
        <li><span class=hl>B</span> - same but from bottom to top</li>
        <li><span class=hl>C</span> - add the first and last stack elements</li>
        <li><span class=hl>D</span> - add the first and second stack elements together</li>
        <li><span class=hl>E</span> -  send the top stack value to Caesar</li>
        <li><span class=hl>F</span> - send the bottom stack value to Caesar</li>
        <li><span class=hl>G</span> - remove the top value from the stack</li></ul>
</p>
<p><h2>Syntacic quarks</h2>
Every command <b>MUST END WITH SEMICOLON!</b> Quotes do nothing here, this language is <b>weakly typed without type declaration.</b>
The langage supports multiline commands, which means that this code is valid:<br>
<span class="hl">save hello<br/>world; yell;</span><br>
There are <b>no codeblocks</b> in this language, so <br>
<span class="hl">if 5 {yell; yell;} #invalid;
    <br> if 5 yell; yell; #invalid;
    <br>if 5 yell; if 5 yell; #valid;
</span><br>
Entered argument <span class="hl">x</span> cannot contain spaces, but memory can.<br>
comments are regarded as <b>regular commands, so they must end in semicolon.</b><br> 
<span class="hl">
    #valid;<br>
    #invalid<br>
    #valid<br>
</span>
Also, the code isnt interpreted in real time, instead it shows output after it's finished running.
<br><b>The program allows up to 5000 iterations</b><br>The default value of memory is <b>non</b>
</p>
<p>
    <h2>Example code</h2>
    Hello world:<br>
    <span class="hl">save Hello World;<br>yell;</span><br>
    <br>cat:<br>
    <span class="hl">listen;<br>yell;</span>
    <br>
    <br>truth-machine:<br>
    <span class="hl">if non listen;<br>
        if 0 yell;<br>
        if! 0 yell;<br>
        if! 0 move;</span>

<br>addition of two numbers:<br>
<span class="hl">if non listen;
    listen;<br>
    signal;<br>
    listen;<br>
    signal;<br>
    raise D;<br>
    yell;<br></span>
</p>

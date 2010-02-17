About
=====

Erlang libiconv binding (uses the new NIF api).

Compiling
=========

Set ERL_TOP environment variable and run make:

<pre>
export ERL_TOP=/path/to/otp/clone
make
</pre>

Using
=====

<pre>
make shell

Eshell V5.7.5  (abort with ^G)
1> CD = iconv:open(&lt;&lt;"ucs-2be"&gt;&gt;, &lt;&lt;"utf-8"&gt;&gt;).
&lt;&lt;96,31,138,2,0,0,0,0&gt;&gt;>>
2> iconv:iconv(CD, &lt;&lt;"text"&gt;&gt;).
{ok,&lt;&lt;0,116,0,101,0,120,0,116&gt;&gt;}
3> iconv:close(CD).
ok
</pre>
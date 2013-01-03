Tinywebserver - Toy web servers based on different concurrent models
=================================================================

Tinywebserver, implements three kinds of web servers, aims to benchmark the performance of concurrent models - prefork, multi-thread, and IO-multiplex.
Tinywebserver is built upon the demo program in the textbook [Computer Systems: A Programmer's Perspective](http://csapp.cs.cmu.edu/), and extends to the multi-thread and epoll models.

Tinyserver is by no means a production software. However, it surpports a number of basic functions, e.g. handling requests of plain text, html, jpeg, gif, and cgi.

* Install:
    
        $ cd src/
        $ make

If installed correctly, three tinyservers would be generated, tinyserver_prefork, tinyserver_thread, and tiny_epoll, respectively. 
In addition, a demo cgi program would be built in the directory cgi-bin.

* Uninstall
    
        $ make clean


* Usage

    * To start. ./tinyservername port. For example, 
    
            $ ./tinyserver_prefork 8000
    
    * To stop.
    
            $ Ctrl+C
    

    * Typing URL in your browser.
        * request for static webpages, type URL directly, e.g. http://localhost:8000/
        * request for cgi, you can reach it directly by setting its parameters, e.g. http://localhost:8000/cgi-bin/adder?4&2. Alternatively, reaching it via its corresponding form page, e.g. adder.html 

* Benchmark using third-party facilities
Each tinyserver program could be benchmarked by regular test tools, e.g. [Apache AB](http://httpd.apache.org/docs/2.2/programs/ab.html) 


enjoy!

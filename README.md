# Tinyhttpd

Tinyhttpd学习加注释；
参考：cbsheng/tinyhttpd、EZLippi/Tinyhttpd;

首先就是服务器的理解：运行服务器程序，是一个数据库；比如Tinyhttpd里面及只有一个网页可以访问index.html;但是你同样可以在这个服务器中添加自己的网页，但是也自己写一个cgi程序来解释；Tinyhttpd里面的cgi脚本是用Perl脚本写的，你其实也可以用c来写的，明白原理就能够写的。在html里面指定了action，即cgi程序。同时也指定了method，即GET，POST等。

客户端<---->服务器<---->cgi程序；在Tinyhttpd中，是在服务器程序中打开一个子进程，来exec相应的cgi程序。具体处理可查看Tinyhttpd的程序，以及印象笔记里面相关的blog。

    liaohua

以下内容来自源作者:

This software is copyright 1999 by J. David Blackstone. Permission is granted to redistribute and modify this software under the terms of the GNU General Public License, available at http://www.gnu.org/ .

If you use this software or examine the code, I would appreciate knowing and would be overjoyed to hear about it at jdavidb@sourceforge.net .

This software is not production quality. It comes with no warranty of any kind, not even an implied warranty of fitness for a particular purpose. I am not responsible for the damage that will likely result if you use this software on your computer system.

I wrote this webserver for an assignment in my networking class in 1999. We were told that at a bare minimum the server had to serve pages, and told that we would get extra credit for doing "extras." Perl had introduced me to a whole lot of UNIX functionality (I learned sockets and fork from Perl!), and O'Reilly's lion book on UNIX system calls plus O'Reilly's books on CGI and writing web clients in Perl got me thinking and I realized I could make my webserver support CGI with little trouble.

Now, if you're a member of the Apache core group, you might not be impressed. But my professor was blown over. Try the color.cgi sample script and type in "chartreuse." Made me seem smarter than I am, at any rate. :)

Apache it's not. But I do hope that this program is a good educational tool for those interested in http/socket programming, as well as UNIX system calls. (There's some textbook uses of pipes, environment variables, forks, and so on.)

One last thing: if you look at my webserver or (are you out of mind?!?) use it, I would just be overjoyed to hear about it. Please email me. I probably won't really be releasing major updates, but if I help you learn something, I'd love to know!

Happy hacking!

                               J. David Blackstone

## What is the Berry language???

Berry is a simple, reliable and straightforward fork of Ruby, with similar features and more. It's extremely portable (works on Windows, OSX and many other OS's), it has a simple syntax and is frequently updated.

Can I contribute?
YES! If you want to update anything, or do anything, please work your magic! We will usually accept your requests, as long as the change you make is worth while, and makes sense. One of the reasons we created this was to pull the language in a similar but different, open direction to ruby.

How do I install Berry?
*
Please note that if you want to use Visual C++ to compile Berry, read win32/README.win32 instead.
You may also have to be a super user for installation to work.
*

1.  Run `./configure`, which will generate config.h and Makefile.

    Some C compiler flags may be added by default depending on your
    environment.  Specify `optflags=..` and `warnflags=..` as necessary to
    override them.

2.  Edit `defines.h` if you need. Usually this step will not be needed.

3.  Remove comment mark(`#`) before the module names from `ext/Setup` (or add
    module names if not present), if you want to link modules statically.

    If you don't want to compile non static extension modules (probably on
    architectures which do not allow dynamic loading), remove comment mark
    from the line "`#option nodynamic`" in `ext/Setup`.

    Usually this step will not be needed.

4.  Run `make`.

5.  Optionally, run '`make check`' to check whether the compiled Ruby
    interpreter works well. If you see the message "`check succeeded`", your
    ruby works as it should (hopefully).

6.  Run '`make install`'

    This command will create the following directories and install into them.

    *   `${DESTDIR}${prefix}/bin`
    *   `${DESTDIR}${prefix}/include/ruby-${MAJOR}.${MINOR}.${TEENY}`
    *   `${DESTDIR}${prefix}/include/ruby-${MAJOR}.${MINOR}.${TEENY}/${PLATFORM}`
    *   `${DESTDIR}${prefix}/lib`
    *   `${DESTDIR}${prefix}/lib/ruby`
    *   `${DESTDIR}${prefix}/lib/ruby/${MAJOR}.${MINOR}.${TEENY}`
    *   `${DESTDIR}${prefix}/lib/ruby/${MAJOR}.${MINOR}.${TEENY}/${PLATFORM}`
    *   `${DESTDIR}${prefix}/lib/ruby/site_ruby`
    *   `${DESTDIR}${prefix}/lib/ruby/site_ruby/${MAJOR}.${MINOR}.${TEENY}`
    *   `${DESTDIR}${prefix}/lib/ruby/site_ruby/${MAJOR}.${MINOR}.${TEENY}/${PLATFORM}`
    *   `${DESTDIR}${prefix}/lib/ruby/vendor_ruby`
    *   `${DESTDIR}${prefix}/lib/ruby/vendor_ruby/${MAJOR}.${MINOR}.${TEENY}`
    *   `${DESTDIR}${prefix}/lib/ruby/vendor_ruby/${MAJOR}.${MINOR}.${TEENY}/${PLATFORM}`
    *   `${DESTDIR}${prefix}/lib/ruby/gems/${MAJOR}.${MINOR}.${TEENY}`
    *   `${DESTDIR}${prefix}/share/man/man1`
    *   `${DESTDIR}${prefix}/share/ri/${MAJOR}.${MINOR}.${TEENY}/system`



## Copying

See the file `COPYING`.

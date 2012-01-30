java2python
-----------

Simple but effective tool to translate Java source code into Python.


There are [lots of docs](./doc/index.md), [plenty of tests](./test), and [many options](./doc/customizations.md) for controlling code generation.

I'm in the process of finalizing the documentation and packaging a release.  That will be release 0.5 when it's done.  If you're looking for old releases, check the [downloads](downloads) link above.

Hello, world example:

    $ cat HelloWorld.java
    // This is the HelloWorld class with it's single method.
    class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello, world.");
        }
    }

    $ j2py HelloWorld.java
    #!/usr/bin/env python
    """ generated source for module HelloWorld

    """
    #  This is the HelloWorld class with it's single method.
    class HelloWorld(object):
        """ generated source for class HelloWorld

        """
        @classmethod
        def main(cls, args):
            """ generated source for method main

            """
            print "Hello, world."


    if __name__ == '__main__':
        import sys
        HelloWorld.main(sys.argv)


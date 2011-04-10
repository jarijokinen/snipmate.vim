snipmate.vim fork with "to uppercase" methods
=============================================

This fork to [snipmate.vim](https://github.com/msanders/snipmate.vim) plugin adds %uc() and %ucfirst() methods that you can
use in your snippets.

Method %uc() converts the string to uppercase, method %ucfirst() converts only
the initial character.

The conversion is not done in real time - it's done after you "quit" the
snippet using arrow keys or tab.

Example
-------

Snippet:

    snippet dc
      def create
        @${1:product} = %ucfirst($1).new
        %uc($1) = "This is Ruby %uc(constant) example."
      end

Output:

    def create
      @product = Product.new
      PRODUCT = "This is Ruby CONSTANT example."
    end

Plugin installation
-------------------

Quickly install with:

    git clone git://github.com/jarijokinen/snipmate.vim.git
    cd snipmate.vim
    cp -R * ~/.vim

# Ruby AST Visualizer [![Gem Version](https://badge.fury.io/rb/ruby_ast_visualizer.svg)](http://badge.fury.io/rb/ruby_ast_visualizer)

Ruby AST Visualizer. Based on [Parser](https://github.com/whitequark/parser).

## Install

```sh
$ gem install ruby_ast_visualizer
```

## Usage

An example `ruby_ast_visualizer` command.

```sh
$ cat hello.rb
puts 'hello, world'
$ ruby_ast_visualizer hello.rb

(send nil :puts
  (str "hello, world"))

Wrote a.png
```

or

```sh
$ ruby_ast_visualizer -e 'puts "hello, world"'

(send nil :puts
  (str "hello, world"))

Wrote a.png
```

AST image file is generated.

<img src="https://raw.githubusercontent.com/koic/ruby_ast_visualizer/master/images/hello_world.png" alt="hello, world"/>

### A little more in detail

You can specify output path in the `-o` option. That value is default a.png.

```sh
$ ruby_ast_visualizer -o path/to/file -e 'puts "hello, world"'

(send nil :puts
  (str "hello, world"))

Wrote path/to/file
```

And you can also specify the `-n` (`--no-image`) option if you don't need an image.
You can only get the result of S-expression by Parser gem.

```sh
$ ruby_ast_visualizer -n -e 'puts "hello, world"'

(send nil :puts
  (str "hello, world"))
```

## Requirements

* Graphviz

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Ruby AST Visualizer is released under the GNU General Public License, version 2.

# Command Line Interfaces

These programs are run from the terminal or command prompt. They could have graphical interfaces too, but they're generally for being used as development tools alongside an editor and other commands.

Building out command line interfaces (CLIs) are great for learning a new language because you don't have to worry about the graphical interface and visual design. You can instead focus on the interactions and the work the program does. This simplifies things quite a bit. It also lets you learn a language's standard library and even third-party packages well. 

If you use a lot of command line apps, then I imagine you'll be drawn to writing them. It's a lot of fun. And no matter how simple it is, all that matters is that it's useful. The Unix philosophy of small programs that can be chained together is really great for learning and building tools and commands.

## Mindset / Targets

Pretty much any language you want to work will have some way of writing command line apps, from Ruby to Python to Node.js to C to Rust to Go. Especially when it comes to learning, you can just go for it and not worry much about technology choices.

But I think certain languages are better candidates for command line apps than others. Specifically languages that compile to a small, portable binary that's easy to install for users. 

Let me break that down a bit more.

Let's take Ruby for example. Ruby is a scripting language that requires an installation of Ruby to be present to run. This means that if I write a Ruby program, for you to run it, you need to have Ruby installed. Or I need to package Ruby up and distribute it with the program. Ruby (and most programming languages) aren't small and super portable, so that's not really that fun. And installing Ruby is kind of a pain in the butt.

You know what'd be nice? If I could just provide you with a single file that you could run. And hopefully that file is pretty small. I don't want to waste your disk space or anything.

Well, that's what's called compiling down to a binary. The binary file is a packaged up version that can run on a lot of different computer operating systems without needing to have the language installed. Yay! Go and Rust in particular are really fantastic at this. You run some commands to compile the program and it can be used by others on the same OS as you. And it's not too difficult to generate it for other operating systems either.

So, it's not that Ruby isn't good for writing CLIs. I think the opposite! It's got a great standard library for it, and I find it quite intuitive and fun, especially for smaller scripts. Using Ruby for a CLI is great if you want to learn Ruby and that sort of programming. But it's not great for building programs you want to distrubte to others unless you know they will also have Ruby installed.

If I was to take on a CLI project, I'd likely choose Rust or Go because I know it'd be possible to build and distribute the compiled version cross-platform.

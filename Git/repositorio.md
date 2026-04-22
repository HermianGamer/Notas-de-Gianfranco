A [[Git]] repository** (often shortened to "repo") is ==the central storage unit of a project managed by [Git](https://git-scm.com/)==, an open-source distributed version control system. It contains every [[File]] and [[Directory]] in your [[project]], along with a full history of every change made since its creation.

All the data in a Git repository is stored directly in the (hidden) `.git` directory. That includes all the commits, branches, tags, and other objects we'll learn about later.

Git is made up of [objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects) that are stored in the `.git/objects` directory. A commit is just a type of object.

para eliminar un repositorio solo es necesario usar `rm .git` del proyecto
Adding a [[Remote]] to our Git repo does _not_ mean that we automagically have all the contents of the remote. First, we need to fetch the contents.

## Assignment

Before fetching the data itself, let's take a look at the new empty repo's `.git/objects` directory with `find`.

```bash
find .git/objects
```

_It should be eerily empty with only 3 entries because we haven't fetched anything yet._

Just because we fetched all of the metadata from the remote `webflyx` repo doesn't mean we have all of the files.

# Making Fetch Happen

Now, to bring the remote `webflyx` [[repositorio]]'s info into our `webflyx-local` repo, we have to [fetch](https://git-scm.com/docs/git-fetch) it.

## Command

```bash
git fetch
```

This downloads copies of all the contents of the `.git/objects` directory (and other bookkeeping information) from the remote repository into your current one.

# Not Fetched

Just because we fetched all of the metadata from the remote `webflyx` repo doesn't mean we have all of the files.
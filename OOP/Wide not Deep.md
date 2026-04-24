It's more common for an [[Inheritance Hierarchy]] tree to be wide than deep.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/R95oIGp-925x500.png)

In your application code, you likely won't see a `Camera` class inherit from a chain of 13 classes up to `Equipment`. If you do: _run_. There are better organizations to work for, I swear.

## Why Wide Not Deep?

A child class is a _strict subset_ of its parent class. In a deep tree, that means the children need to be perfect members of all the parent class "types". That just doesn't happen very often. It's more likely that you'll have a base class that simply has many child classes that are slightly different variations of the base. They're all "siblings" of each other.
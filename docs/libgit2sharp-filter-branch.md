An idiomatic c-sharpy API for doing filter-branch-like operations. It never touches the index or working directory, so it's probably wicked fast.

The API is rather nice to work with:

```csharp
repo.Branches.RewriteHistory(
	// A collection of commits that should be rewritten
	repo.Head.Commits,

	// A function that returns a `TreeDefinition` for the new commit
	commitTreeRewriter: c =>
		{
			var td = TreeDefinition.From(c);
			td.Remove("README");
			return td;
		},

	// A function that returns header information to be used for the new commit
	commitHeaderRewriter: c =>
		{
			var ch = CommitHeader.From(c);
			ch.Message += "\n\nCleaned-by: The Cleaner";
			return ch;
		});
```

As of the end of hack day, it's [not quite ready to merge](https://github.com/libgit2/libgit2sharp/pull/429), but it's surprisingly compact and featureful.

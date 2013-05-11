Githooks aims to be a simple package manager for git hooks (other suggested name: ghundle). It should also provide tools to run hooks in isolation and test them. The project is written in Ruby, the author is [@AndrewRadev](https://github.com/AndrewRadev), and the repo is [AndrewRadev/githooks](https://github.com/AndrewRadev/githooks).

The tentative API at time of inception is as follows:

List all hooks, installed in the project:

    $ githooks list

    # result:

    post-merge/rails-migrations :: AndrewRadev/githooks-storage/rails-migrations
      Runs `rake db:migrate` if any new migrations were added.

    post-merge/ruby-bundler :: AndrewRadev/githooks-storage/ruby-bundler
      Runs `bundle install` if Gemfile.lock was changed.

    post-checkout/rebuild-ctags :: AndrewRadev/githooks-storage/rebuild-ctags
      Rebuilds project tags upon changing branches.

Install a new hook:

    $ githooks install username/reponame/path/to/hook

Run a hook manually (it would probably need some environment variables to work):

    $ githooks run post-merge/rails-migrations

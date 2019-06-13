# phx-scaffold-spike

https://wsmoak.net/2015/07/27/adding-fields-to-an-ecto-model-in-phoenix.html
```
After discovering that I needed to add some fields to the User model, 
I checked to see if there was something like rails generate migration NAME [field[:type]...].
```

## Acceptable outcomes:
1) learn the command to `mix ecto.gen.html.migrate`
2) look at db:schema, and/or db tables for database. Build scaffold commands and teardown commands.
3) create the mix ecto.gen.html.migrate command.
4) create a mix package to analyze and build scaffold and teardown commands.
5) create a npm bash package to analyze and build scaffold and teardown commands.

```bash
psql -d my_app_dev -c "\d+ users"
```

```elixir
mix ecto.gen.migration add_fields_to_users
# for reference suggested looking at: vi priv/repo/migrations/$(ls priv/repo/migrations/ | tail -2)
vi priv/repo/migrations/$(ls priv/repo/migrations/ | tail -1)
```

Other files to modify:
```elixir
# web/templates/user/show.html.eex
# web/models/user.ex
# web/page_controller.ex
```

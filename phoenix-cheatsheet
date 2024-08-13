# Create database with Ecto
`$ mix ecto.create`

# Run ecto migration
`$ mix ecto.migrate`

# Generate ecto migration
`$ mix ecto.gen.migration create_product_categories`
then edit corresponding migration file. Example:

```
defmodule Hello.Repo.Migrations.CreateProductCategories do
  use Ecto.Migration

  def change do
    create table(:product_categories, primary_key: false) do
      add :product_id, references(:products, on_delete: :delete_all)
      add :category_id, references(:categories, on_delete: :delete_all)
    end

    create index(:product_categories, [:product_id])
    create unique_index(:product_categories, [:category_id, :product_id])
  end
end
```


# Run phoenix server
`$ mix phx.server`
or running phoneix server in interactive mode
`$ iex -S mix phx.server`

# Print all routes at router.ex to console
`$ mix phx.routes`

# Generate schema
`mix phx.gen.schema User users name:string email:string bio:string number_of_pets:integer`

# Generate context
```
$ mix phx.gen.html Accounts User users name:string
$ mix phx.gen.json Accounts User users name:string
$ mix phx.gen.live Accounts User users name:string
$ mix phx.gen.context Accounts User users name:string
```
The context serves as the API boundary for the given resource.
Multiple resources may belong to a context and a resource may be
split over distinct contexts (such as Accounts.User and Payments.User).




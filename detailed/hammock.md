# Hammock
Leisurely build Restful APIs that serve JSON, protocol buffers, ...

# Useageness
Put a Schema document in the `resources` folder. That's it. You now have all the basic CRUD actions at `/resource_name`.

For example, if you put this in `resources/coconut.rb`:

```ruby
class Coconut
  field :name, type: String
  field :juicy, type: Boolean
end
```

... you get all these routes for free:

- `GET /coconuts` to get all the coconuts
- `GET /coconuts/524a87a7e0f3fc1d2d000001` to get that specific coconat
- `POST /coconuts, { coconut: { name: 'Mr. Brown', juicy: true } }` to create a new coconut
- `PUT /coconuts/524a87a7e0f3fc1d2d000001, { name: 'Nutty' }` to update the coconut
- `DELETE /coconuts/524a87a7e0f3fc1d2d000001` to disintegrate that coconut

Bonus route:

- `POST /coconuts/search, { juicy: true }` to find all the juicy coconuts

# Not Implemented yet
- testing! (how do you do you use rack-test with this?)
- Search
- nested resources (meh.)
- (O)auth

# Furter thoughts
- can this be standardised enough so that a JSON api browser can be built?
  - serve Schema files:
    - validations + error messages
    - names of fields
  - from the schema files:
    - generate forms
    - generate API docs

vva_connect
===

Example Usage
-------------

```ruby
require 'vva'

v = VVA::Services.new.new(
  wsdl: "http://service.example.com?wsdl",
  username: "USER111",
  password: "SECRET",
  ssl_cert_file: "/path/to/cert",
  ssl_cert_key_file: "/path/to/private/key",
  ssl_ca_cert: "/path/to/ca/file"
)

# get document list by claim number
v.document_list.get_by_claim_number("777")

# get document content by document id
v.document_content.get_by_document_id(
  document_id: "{DAFE0879-C588-4084-A532-482138F30651}",
  source: "P8",
  format: "pdf",
  jro: "459",
  ssn: "111111111"
)
```

## Development

After checking out the repo, run `bundle install` to install dependencies. You can also run `bundle console` for an interactive prompt that will allow you to experiment. If you want to use `pry`, run `bundle config console pry` and then `bundle console`.

License
=======

[The project is in the public domain](LICENSE.md), and all contributions will also be released in the public domain. By submitting a pull request, you are agreeing to waive all rights to your contribution under the terms of the [CC0 Public Domain Dedication](http://creativecommons.org/publicdomain/zero/1.0/).

This project constitutes an original work of the United States Government.

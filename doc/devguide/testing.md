## Testing Crowbar

The Dell Crowbar team believes in testing!  We want you to write tests for your code and include it in your pull requests.

We have several mechanisms for testing and the following sections will help you understand them, use them and love them.

### Automated tests

* Unit tests - these validate core logic assumptions in the models and controllers
   * they are written in Ruby and are integrated with the Rails framework
   * they are tightly coupled to the code of the system
   * they are currently implemented in two forms:
      * [tests under `crowbar_framework/test/unit/`, based on Test::Unit](testing/units.md)
      * [tests under `crowbar_framework/spec/`, based on RSpec](testing/rspec.md)
   * RSpec is the preferred framework for new tests, due to its popularity and high quality integration with the rest of the Rails ecosystem (e.g. [guard](https://github.com/guard/guard) and [spork](https://github.com/sporkrb/spork)).
* [Behaviour-Driven Development (BDD) tests](testing/bdd.md)
   * these are system integration tests that exercise the web UI without any integration to the code

It is recommended to [run these automated tests via the `./dev` tool](testing/devtool.md).

### Code coverage reports

Code coverage reports are automatically generated when the tests are
run, and can be accessed via the Rails app's webserver at e.g.
http://192.168.124.10:3000/coverage/ - see [here](testing/web-ui.md)
for how to start the web server.

### Manual tests

* [Testing the web UI](testing/web-ui.md)

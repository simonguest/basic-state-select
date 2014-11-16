basic-state-select
==================

A Web component (written using [Polymer](http://www.polymer-project.org)) that provides a basic control for showing a list of the 50 states in the US.

Attributes applied to the control can determine the default state chosen, the select text, and whether the select text is removed from the menu when a state is selected.

The element also exposes an event called stateChanged, which can be used to determine if a state has been selected.

##Installation

Perform an bower install in order to install the required dependencies:

    bower install basic-state-select

##Usage

To use, import the required basic-state-select.html reference, and create a new tag:

    <!DOCTYPE html>
    <html>
      <head>
          <link rel="import" href="/bower_components/basic-state-select/basic-state-select.html">
      </head>
      <body>
        <basic-state-select id="states"
                            selectText="Please select..."
                            defaultState="CA"
                            removeSelectValue="true"></basic-state-select>
      </body>
      <script>
        var states = document.getElementById('states');
        states.addEventListener('stateChanged', function(e) {
            console.log('state was changed to '+ e.detail.state);
        });
      </script>
    </html>

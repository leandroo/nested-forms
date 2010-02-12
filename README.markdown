Nested Forms
============

jQuery plugin making it incredibly easy to implement rich behavior for your nested forms in Rails.

All you have to do is have at least one instance of the nested form on the page (visible or not) and you're set.

[Source](http://github.com/andyferra/nested-forms)


Features:
---------

- Really smart defaults
- Super flexible
- Supports nested forms inside nested forms
- Event Callbacks (after_add, after_remove)
- CSS class cycling (defaults to 'odd', 'even') (can be customized / disabled)
- Keyboard Shortcuts (SHIFT-ENTER to add) (can be disabled)
- Automatic focus on first field of added items (can be customized / disabled)
- 3.3K Uncompressed


Simple Example
--------------

### HTML ###

    <div id="people">
      <div class="person">
        <form><!-- nested form --></form>
        <a href="#remove_person">Remove</a>
      </div>
      <a href="#add_person">Add</a>
    </div>

### Javascript ###

    $('.people').has_nested_forms('.person');


Nested, Nested Example
----------------------

### HTML ###

    <div class="people">
      <div class="person">
        <form><!-- nested form --></form>
        <a href="#remove_person">Remove</a>

        <div class="hobbies">
          <div class="hobby">
            <form><!-- nested, nested form --></form>
            <a href="#remove_hobby">Remove</a>
          </div>
          <a href="#add_hobby">Add</a>
        </div>

      </div>
      <a href="#add_person">Add</a>
    </div>

### Javascript ###

    $('.people').has_nested_forms('.person');
    $('.hobbies').has_nested_forms('.hobby', { depth: 2 });


See [defaults object](http://github.com/andyferra/nested-forms/blob/master/jquery-nested-forms.js#L22) in the plugin for a full list of options.

# sfCkPlugin

The `sfCkPlugin` offers unobtrousive integration for symfony and the js-based WYSIWYG editor CK.

## Installation and configuration

### Installation

Use the default plugin installer procedure

    php symfony plugin:install sfCkPlugin


### Configuration

Enable the plugin in your projectConfiguration class:

    public function setup()
    {
      $this->enablePlugins('sfCkPlugin');
    }

publish plugin's assets:

    php symfony plugin:publish-assets

add plugin's JS to the application or module you want to use it into.

For example, if I want to use CK for all the teaxtareas of my backend, I'd edit

    apps/backend/config/view.yml

with the following code:

    javascripts:    [/sfCkPlugin/js/sfCkPlugin.js]

Then [download the editor's package](http://ckeditor.com/ "CKEditor website"), put the *ckeditor* folder under:

    web/js/

and enable the editor package where you want to have CKEditor enabled ( for example, the already-discussed view.yml ):

    // apps/backend/config/view.yml
    javascripts:    [ckeditor/ckeditor,/sfCkPlugin/js/sfCkPlugin.js]

You're done!

### Unobtrousive... and flexible!

If you want to disable the CKeditor in a textarea widget you only need to pass it the *no-editor* class:

    $this->widgetSchema['myTextarea'] = new sfWidgetFormTextarea(array(), array('class' => 'no-editor'));
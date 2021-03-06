sfSlovenianPlugin
=================

Slovenian translations of core Symfony messages (required, yes or no, is empty, etc).

Symfony does not include message catalogues for its own messages.
However Doctrine and Propel plugins include translations for their messages under the 'sf_admin' catalogues,
so they are not found by Symfony core classes which look only under the 'messages' catalogue.
The misleading issue is that if you use Doctrine or Propel to generate your filter forms,
you get almost everything translated, but the core Symfony widgets messages are not translated.
The solution is to create a messages.[LANG].xml in [pathToProject]/apps/[appName]/i18n/ for the core Symfony library or use this plugin for Slovenian language.


Installation
------------

* Install the plugin (via a package)

        $ symfony plugin:install sfSlovenianPlugin


* Or install the plugin

        $ svn co http//svn.symfony-project.com/plugins/sfSlovenianPlugin/trunk plugins/sfSlovenianPlugin


* Activate the plugin in the `config/ProjectConfiguration.class.php`

        [php]
        class ProjectConfiguration extends sfProjectConfiguration
        {
          public function setup()
          {
            $this->enablePlugins(array(
              '...',
              'sfSlovenianPlugin',
              '...'
            ));
          }
        }


* Clear the cache

        $ symfony cache:clear


* enable i18n in `apps/[appName]/config/settings.yml`

        i18n: true


* set default culture `apps/[appName]/config/settings.yml` if it has not been otherwise defined

        default_culture: sl_SI



TODO
----

* check for missing translations

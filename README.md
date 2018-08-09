# This is a plugin for UBC Wiki.

This plugin is adding additional license messages to upload wizard to satisfy UBC legal requirements.

### Notes

Mediawiki use wfMessage() for PHP and mw.msg() for JS to handle i18n translation. It seems on the PHP side, wfMessage can handle cross extension string loading. But mw.msg() use load.php with modules parameter to load only specific modules i18n messages. So in order to customize the text in UploadWizard license text, we have to modify the extension i18n files and extension.json file to include messages. (we can't use a separate extension to inject the i18n messages) 

The messages can be override by on-wiki text: https://www.mediawiki.org/wiki/Special:AllMessages

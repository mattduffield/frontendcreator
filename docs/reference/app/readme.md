# Application Reference

The following is a listing of settings or values used within **Frontend Creator**.

## Support File Extensions
**Frontend Creator** uses the Monaco Editor. It examines the the file extension and determines if it is a supported type for use. The following is a listing of the extension types **Frontend Creator** uses internally.

In order to support even unknown text types not listed below, **Frontend Creator** uses reverse logic allowing for anything that is not Image or Font to be used as a text type and rendered in the editor. 

If a file extension is encountered that is not an Image or File but does not belong to the list of known extensions, then we use `text/plain` as the default language for the Monaco Editor.

### Text File Extensions
The following is a list of file extensions currently listed for support with Monaco Editor:

- 'coffee',
- 'cs',
- 'css',
- 'csv',
- 'gitignore',
- 'go',
- 'htm',
- 'html',
- 'ini',
- 'js',
- 'json',
- 'jsx',
- 'md',
- 'php',
- 'ps',
- 'py',
- 'rtf',
- 'sh',
- 'spec',
- 'sql',
- 'svg',
- 'ts', 
- 'tsx', 
- 'txt',
- 'vb',
- 'xml',
- 'yaml'

## Image File Extensions
The following is a list of file extensions known to be images files:

- 'ico',
- 'jpeg',
- 'jpg',
- 'gif',
- 'png',
- 'bmp'

## Font File Extensions
The following is a list of file extensions known to be font files:

- 'otf',
- 'eot',
- 'ttf',
- 'woff',
- 'woff2'


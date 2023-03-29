# MIR and FSCA XML Format Guide
Use this guide if you want to create your own MIR or FSCA XML files.
You'll need to follow these instructions to ensure that the files validate against the schema, and are fully compatible with the websites listed in the [README](README.md).

## The XML root element
The XML root element is described in the various schema (`<incident>` for the MIR form, and `<fsca>` for the FSCA form).

These elements will need to reference the schema and some other data as follows:

### MIR Report Form
For the MIR report form, for the `<incident>` root element:

- set the xsi namespace (`xmlns:xsi`) attribute to the usual W3C XML schema instance `"http://www.w3.org/2001/XMLSchema-instance"`;
- set the `xsi:noNamespaceSchemaLocation` attribute to the relevant XML schema, for instance `"incident-Initial-v7.2.1.xsd"`;
- set the `version` attribute to `"V5.0 2018-05-30"`;
- set the `sCreateTimeStamp` attribute to a valid [ISO-8601 UTC time](https://www.utctime.net/) for the time you created to file, e.g. `"2023-03-29T14:27:33"`;
- set the `sFormLanguage` language to a suitable [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) language code, e.g. `"en"`.

For example:
```
<incident xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="V5.0 2018-05-30" xsi:noNamespaceSchemaLocation="incident-Initial-v7.2.1.xsd" sCreateTimeStamp="2023-03-29T14:27:33" sFormLanguage="en">
```

### FSCA Report Form
For the FSCA  report form, for the `<fsca>` root element:

- set the xsi namespace (`xmlns:xsi`) attribute to the usual W3C XML schema instance `"http://www.w3.org/2001/XMLSchema-instance"`;
- set the `xsi:noNamespaceSchemaLocation` attribute to the relevant XML schema, for instance `"FSCA_Initial_v2.6.xsd"`;
- set the `version` attribute to `"V2.7 2012-12-03"`.

For example:
```
<fsca xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="V2.7 2012-12-03" xsi:noNamespaceSchemaLocation="FSCA_Initial_v2.6.xsd">
```



# Validating Your XML
To validate your XML, you'll need an editor or IDE that performs schema validation or another validation tool, such as:

- Microsoft VSCode, using an XML extension such as XML Language Support by Red Hat;
- Notepad++, using and XML validation extension such as XML Tools;
- an online tool; or
- a tool from https://www.w3.org/wiki/XML_Schema_software.

Ensure your XML file is in the same directory as the schema and open it with your tool of choice.
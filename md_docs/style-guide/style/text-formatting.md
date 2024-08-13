---
title: Text Formatting
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/text-formatting/
---

# Text Formatting

You should add formatting to words, phrases, or blocks that require emphasis. You can use one of the formatting options to convey emphasis: weight (**bold**), variant (*italics*), or pitch (`monospace`).

When formatting text, use the following guidelines:

- To apply a font treatment, use the appropriate markup in your authoring tool. In reStructuredText, use a role or directive if one is available.

- Don't apply emphasis to text in titles and headings. An exception would be if a title of a page or a heading of a section covers some code or command.

- Don't change the case of the text to emphasize a term. This includes showing a general term in all capitals, small capitals, or initial capitals. If you are representing all-cap text from the user interface, write it as initial cap instead.

- Don't use color to distinguish text.

- Use quotation marks only as directed in this topic and in Quotation marks.

The following table shows the text formatting to use for different text elements. The following style differences are highlighted:

- Content that documents a CLI or API versus a GUI

Apply no additional formatting.

Product Names.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
You must configure MongoDB Compass.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
You must configure MongoDB Compass.

</td>
</tr>
</table>Format using `:guilabel:` role and capitalize the first letter of each word.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Edit Signature` area, enter the text that
you want to appear in your signature.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Edit Signature area, enter the text that you want to appear in your signature.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
To list or retrieve files from a node that's running the
OpenCenter agent, use the ``file`` argument with the
``opencentercli`` node command.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
To list or retrieve files from a node that's running the OpenCenter agent, use the `file` argument with the `opencentercli` node command.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The ``expires`` attribute denotes the time after which
the token automatically becomes invalid.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The `expires` attribute denotes the time after which the token automatically becomes invalid.

</td>
</tr>
</table>This covers check box, combo box, group box, list box, spin box, and text box. Format them using the `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select the :guilabel:`Manually configure server settings
or additional server types` check box.

Retype the password that you entered in the
:guilabel:`Password` box.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select the Manually configure server settings or additional server types check box.

Retype the password that you entered in the Password box.

</td>
</tr>
</table>This covers *command*, *option*, *radio*. Format using the `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select :guilabel:`Microsoft Exchange` and then click
:guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select Microsoft Exchange and then click Next.

</td>
</tr>
</table>- Order by menu, then field.

- Format using the `:guilabel:` role.

- Separate levels with >.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select :guilabel:`Start > Control Panel`, and then
click the :guilabel:`Mail` icon.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select Start > Control Panel, and then click the Mail icon.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select the :guilabel:`Manually configure server settings
or additional server types` check box.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select the Manually configure server settings or additional server types check box.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
``grep "ftp" /etc/xinetd.d/*``
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
`grep "ftp" /etc/xinetd.d/*`

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Sort the backups by server by clicking the
:guilabel:`Server` column label.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Sort the backups by server by clicking the Server column label.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select a name from the :guilabel:`Send to` list, or type
a new name.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select a name from the Send to list, or type a new name.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Check the architecture on Linux by using the
``uname -a`` command.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Check the architecture on Linux by using the `uname -a` command.

</td>
</tr>
</table>Varies by operating system:

<table>

<tr>
<td>
Linux, macOS

</td>
<td>
Format using the `.. code-block:: console` directive.

</td>
</tr>
<tr>
<td>
DOS, Windows Command-Line Interpreter

</td>
<td>
Format using the `.. code-block:: doscon` directive.

</td>
</tr>
<tr>
<td>
Windows Powershell

</td>
<td>
Format using the `.. code-block:: ps1con` directive.

</td>
</tr>
</table>Omit the command prompt if you aren't displaying the response in the same code block.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
If a service isn't running, use the service command to
start it, as follows:

.. code-block:: console
   :copyable: false

   sudo service httpd start

To set your home directory path:

.. code-block:: doscon
   :copyable: false

   SET HOME=<home-directory>

To retrieve your home directory path:

.. code-block:: ps1con
   :copyable: false

   echo $env:HOMEPATH
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
If a service isn't running, use the service command to start it, as follows:

```console
sudo service httpd start
```

To set your home directory path:

```doscon
SET HOME=<home-directory>
```

To retrieve your home directory path:

```ps1con
echo $env:HOMEPATH
```

</td>
</tr>
</table>Format using the `.. code-block:: ini` directive.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
.. code-block:: ini
   :copyable: false

    mmsBaseUrl=http://example.com:8080
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
```ini
 mmsBaseUrl=http://example.com:8080
```

</td>
</tr>
</table>Format using the `.. code-block:: yaml` directive.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
.. code-block:: yaml
   :copyable: false

   ---
   apiVersion: mongodb.com/v1
   kind: MongoDB
   metadata:
     name: <myShardedCluster>
   spec:
     shardCount: 2
     mongodsPerShardCount: 3
     mongosCount: 2
     configServerCount: 3
     version: 4.2.2-ent
     opsManager:
       configMapRef:
         name: <configMap.metadata.name>
               # Must match metadata.name in ConfigMap file
     credentials: <myCredentials>
     type: ShardedCluster
     persistent: true
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
```yaml
---
apiVersion: mongodb.com/v1
kind: MongoDB
metadata:
  name: <myShardedCluster>
spec:
  shardCount: 2
  mongodsPerShardCount: 3
  mongosCount: 2
  configServerCount: 3
  version: 4.2.2-ent
  opsManager:
    configMapRef:
      name: <configMap.metadata.name>
            # Must match metadata.name in ConfigMap file
  credentials: <myCredentials>
  type: ShardedCluster
  persistent: true
```

</td>
</tr>
</table>Links and Cross-References.

Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Start by creating a new database called ``mytestdb``.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Start by creating a new database called `mytestdb`.

</td>
</tr>
</table>Format using the `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Microsoft Exchange` dialog box, click
:guilabel:`Apply` and then click :guilabel:`OK`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Microsoft Exchange dialog box, click Apply and then click OK.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The following example shows a basic configuration for
the FTP service, in a file in the ``/etc/xinetd.d/``
directory.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The following example shows a basic configuration for the FTP service, in a file in the `/etc/xinetd.d/` directory.

</td>
</tr>
</table>Format using *italics*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
For details about code examples, see the "Code examples"
section in the *Microsoft Style for Technical
Publications, 4th Edition*.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
For details about code examples, see the "Code examples" section in the *Microsoft Style for Technical Publications, 4th Edition*.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The ``message`` element returns a human-readable message
that's appropriate for display to the end user.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The `message` element returns a human-readable message that's appropriate for display to the end user.

</td>
</tr>
</table>Format using **boldface**.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
**your.name@example.com**
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
**your.name@example.com**

</td>
</tr>
</table>Apply no additional formatting.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
If you have any questions regarding this agreement or
the backup software, please direct all correspondence
to: legal@mongodb.com.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
if you have any questions regarding this agreement or the backup software, please direct all correspondence to: legal@mongodb.com.

</td>
</tr>
</table>Format using *italics*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Offset *must* be a multiple of the limit (or zero);
otherwise, a Bad Request exception is generated.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Offset *must* be a multiple of the limit (or zero); otherwise, a Bad Request exception is generated.

</td>
</tr>
</table>Varies by operating system:

<table>

<tr>
<td>
Linux, macOS

</td>
<td>
Format using `monospace` text and uppercase letters. Start with `$` when getting, omit the `$` when assigning.

</td>
<td>
```console
HOME=<home-directory>

echo $HOME
```

</td>
</tr>
<tr>
<td>
DOS, Windows Command-Line Interpreter

</td>
<td>
Format using `monospace` text and uppercase letters. Start and end with `%` when getting, omit the `%` when assigning.

</td>
<td>
```doscon
SET HOME=<home-directory>

echo %HOME%
```

</td>
</tr>
<tr>
<td>
Windows Powershell

</td>
<td>
Format using `monospace` text and uppercase letters. Start with `$` when getting and assigning.

</td>
<td>
```ps1con
$env:HOMEPATH='<home-directory>'

echo $env:HOMEPATH
```

</td>
</tr>
</table><table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Copy the binaries into a directory listed in your
``PATH`` variable, such as ``/usr/local/bin`` (Update
``/path/to/the/mongodb-directory/`` with your
installation directory as appropriate.)
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Copy the binaries into a directory listed in your `PATH` variable, such as `/usr/local/bin` (Update `/path/to/the/mongodb-directory/` with your installation directory as appropriate.)

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Export the tenant ID to the ``$account`` environment
variable and the authentication token to the ``$token``
environment variable.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Export the tenant ID to the `$account` environment variable and the authentication token to the `$token` environment variable.

</td>
</tr>
</table>Format using `monospace` text inline. If the format of the error aids in user understanding, use the appropriate `.. code-block::` directive.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
If your comment to an acknowledgement is too long, the
API returns:

``Acknowledgement comment too long. It must not exceed
<number> characters.``
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
If your comment to an acknowledgement is too long, the API returns:

`Acknowledgement comment too long. It must not exceed <number> characters.`

</td>
</tr>
</table>Format using the `.. code-block::` directive with corresponding. Pygment lexer

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
.. code-block:: javascript
   :copyable: false

   db.collection.create_index(
     [
       (<keyAndIndexTypeSpecification>
     ], <options>
   )

.. code-block:: java
   :copyable: false

   collection.createIndex(
     <keyAndIndexTypeSpecification>, <options>
   )
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
```javascript
db.collection.create_index(
  [
    (<keyAndIndexTypeSpecification>)
  ], <options>
)
```

```java
collection.createIndex(
  <keyAndIndexTypeSpecification>, <options>
)
```

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Database Name` field, enter a database
name identifier.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Database Name field, enter a database name identifier.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
To remove the ``vs_quantum-api.cfg`` file from the
``haproxy.d`` directory and retain it, you can move it
to another directory.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
To remove the `vs_quantum-api.cfg` file from the `haproxy.d` directory and retain it, you can move it to another directory.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Use the ``-t`` flag to add a timestamp to the results.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Use the `-t` flag to add a timestamp to the results.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Container names are sorted based on a binary comparison,
a single built-in collating sequence that compares
string data using the ``memcmp()`` function, regardless
of text encoding.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Container names are sorted based on a binary comparison, a single built-in collating sequence that compares string data using the `memcmp()` function, regardless of text encoding.

</td>
</tr>
</table>Format using `:term:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
MongoDB deploys a :term:`replica set` after you click
:guilabel:`Save`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
MongoDB deploys a replica set after you click Save.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Edit Signature` area, enter the text
that you want to appear in your signature.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Edit Signature area, enter the text that you want to appear in your signature.

</td>
</tr>
</table>Format using `:guilabel:` role.

**Exception:** Show window, dialog box, wizard, page, panel, and screen names in regular text unless they need to be distinguished from the surrounding text. In such cases, use bold.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Microsoft Exchange` dialog box, click
:guilabel:`Apply` and then click :guilabel:`OK`.

On the :guilabel:`Choose Service` page, select
:guilabel:`Microsoft Exchange or compatible service`,
and then click :guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Microsoft Exchange dialog box, click Apply and then click OK.

On the Choose Service page, select Microsoft Exchange or compatible service, and then click Next.

Read the preliminary steps in the Configure Your Server wizard, and then click Next.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Avoid putting the ``xml:id`` attribute on the ``title``
tag.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Avoid putting the `xml:id` attribute on the `title` tag.

</td>
</tr>
</table>Links and Cross-References.

Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
To verify which OS version you're running, click the
:guilabel:`Apple` icon in the top-left corner and then
select :guilabel:`About This Mac`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
To verify which OS version you're running, click the Apple icon in the top-left corner and then select About This Mac.

</td>
</tr>
</table>Format using the `:kbd:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Press :kbd:`Shift-G` and then press :kbd:`Enter`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Press Shift-G and then press Enter.

</td>
</tr>
</table>Format using *italics*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Place *i* before *e* except after *c*.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Place *i* before *e* except after *c*.

</td>
</tr>
</table>Links and Cross-References.

Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
From the :guilabel:`Account Type` list, select
:guilabel:`Exchange 2007`.

To view these settings, select
:guilabel:`Configure Backup` from the
:guilabel:`Backup Actions` list.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
From the Account Type list, select Exchange 2007.

To view these settings, select Configure Backup from the Backup Actions list.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Right-click the volume and select
:guilabel:`Take Offline`.

From the :guilabel:`Outlook` menu, select
:guilabel:`Preferences`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Right-click the volume and select Take Offline.

From the Outlook menu, select Preferences.

</td>
</tr>
</table>Format as Cascades.

Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In SQL Server Management Studio, when you right-click a
SQL Server 2012 database and selecting
:guilabel:`Properties`, the following error message
appears:

``The user doesn't have permission to perform this action.``
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In SQL Server Management Studio, when you right-click a SQL Server 2012 database and selecting Properties, the following error message appears:

`The user doesn't have permission to perform this action.`

</td>
</tr>
</table>Format using `monospace` with all capital letters.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Client authentication is provided through a REST
interface by using the ``GET`` method.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Client authentication is provided through a REST interface by using the `GET` method.

</td>
</tr>
</table>Format using `:option:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The size of the oplog is only configurable during the
first run using the ``--oplogSize`` argument to the
:binary:`~bin.mongod` command, or preferably, the
:setting:`~replication.oplogSizeMB` setting in the
MongoDB configuration file. If you do not specify this
on the command line before running with the
:option:`mongod --replSet` option, :binary:`~bin.mongod`
creates a default sized oplog.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The size of the oplog is only configurable during the first run using the `--oplogSize` argument to the `mongod` command, or preferably, the `oplogSizeMB` setting in the MongoDB configuration file. If you do not specify this on the command line before running with the `--replSet` option, `mongod` creates a default sized oplog.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select :guilabel:`Microsoft Exchange` and then click
:guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select Microsoft Exchange and then click Next.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
You must install the ``libvirt`` package.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
You must install the `libvirt` package.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
On the :guilabel:`Preferences` page, you determine how
frequently you receive email about all the activity on
your account: daily, weekly, or both.

On the :guilabel:`Server Settings` page, click
:guilabel:`Check Name`, type your password, and then
click :guilabel:`OK`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
On the Preferences page, you determine how frequently you receive email about all the activity on your account: daily, weekly, or both.

On the Server Settings page, click Check Name, type your password, and then click OK.

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
To verify that your TLS binding works, select your
website in the :guilabel:`Connections` pane (if it's not
already selected) and then click :guilabel:`Browse
ipAddress (https)` in the :guilabel:`Actions` pane.

In the navigation pane, select
:guilabel:`Compose Email`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
To verify that your TLS binding works, select your website in the Connections pane (if it's not already selected) and then click Browse ipAddress (https) in the Actions pane.

In the navigation pane, select Compose Email.

</td>
</tr>
</table>Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The path to Perl is ``#!/usr/bin/perl -w``.

In the URI path
``https://cloud.mongodb.com/api/public/v1.0``, the API
version is 1.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The path to Perl is `#!/usr/bin/perl -w`.

In the URI path `https://cloud.mongodb.com/api/public/v1.0`, the API version is 1.

</td>
</tr>
</table>Apply no additional formatting. Covers file permissions on any operating system.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Log in to a shell as the user who has write permissions
to ``/usr/local/bin`` on your local computer.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Log in to a shell as the user who has write permissions to `/usr/local/bin` on your local computer.

</td>
</tr>
</table>Placeholder or Variable Text.

Apply no additional formatting unless the privilege is an operating system command like `sudo`. Otherwise, you can say elevated privileges.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The following examples assume that you're making the
firewall changes as a normal user with ``sudo``
privileges.

The user is granted ALL privileges on the database.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The following examples assume that you're making the firewall changes as a normal user with `sudo` privileges.

The user is granted ALL privileges on the database.

</td>
</tr>
</table>Format using *italic*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
1. *(Optional)* Enter a new name for the image.

    You can tell that the Managed Cloud post-build
    automation has successfully completed as follows:

    *(Windows servers)* The following file is created:
    **C:\\windows\\temp\\rs\_managed\_cloud\_automation\_complete.txt**

    *(Linux servers)* The following file is created:
    **/tmp/rs\_managed\_cloud\_automation\_complete**
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
1. *(Optional)* Enter a new name for the image.

   You can tell that the Managed Cloud post-build automation has successfully completed as follows:

   *(Windows servers)* The following file is created: **C:\windows\temp\rs_managed_cloud_automation_complete.txt**

   *(Linux servers)* The following file is created: **/tmp/rs_managed_cloud_automation_complete**

</td>
</tr>
</table>Format using Quotation marks, or block quote formatting

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
"Scalability is key for our business," explained Nathan
Goff, Inavero Operations Director and Partner. "There's
nothing worse than making our clients look bad to their
customers."
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
"Scalability is key for our business," explained Nathan Goff, Inavero Operations Director and Partner. "There's nothing worse than making our clients look bad to their customers."

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Select :guilabel:`Microsoft Exchange` and then click
:guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Select Microsoft Exchange and then click Next.

</td>
</tr>
</table>Format using the `:authrole:` or `:atlasrole:` as appropriate for the documented product's roles. Otherwise, format as regular text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The :authrole:`Global Owner` role has the permissions to
create, read, update, and delete resources within
multiple designated products where access is granted.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The `Global Owner` role has the permissions to create, read, update, and delete resources within multiple designated products where access is granted.

</td>
</tr>
</table>Format as Cascades.

Format as Command syntax.

Format using `monospace` text.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
The main command used to change a file’s owner or group
is ``chown``. The most common syntax used with ``chown``
is as follows:

``chown user:group file1 file2 file3``
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
The main command used to change a file’s owner or group is `chown`. The most common syntax used with `chown` is as follows:

`chown user:group file1 file2 file3`

</td>
</tr>
</table>Format using `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Microsoft Exchange` dialog box, click the
:guilabel:`Connection` tab and then select the
:guilabel:`Connect to Microsoft Exchange using HTTP`
check box.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Microsoft Exchange dialog box, click the Connection tab and then select the Connect to Microsoft Exchange using HTTP check box.

</td>
</tr>
</table>Format using *italics*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
MongoDB instances that are built using the base Linux
images are created without a dedicated swap partition
and with *swappiness* (a measure of how the Linux kernel
tries to use swap memory) set to 0.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
MongoDB instances that are built using the base Linux images are created without a dedicated swap partition and with *swappiness* (a measure of how the Linux kernel tries to use swap memory) set to 0.

</td>
</tr>
</table>Don't use.

Format using `:guilabel:` role. If the UI uses all capital letters, change to capitalizing the first letter of each word.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Microsoft Exchange` dialog box, click
:guilabel:`Apply` and then click :guilabel:`OK`.

On the :guilabel:`Choose Service` page, select
:guilabel:`Microsoft Exchange or compatible service`,
and then click :guilabel:`Next`.

Read the preliminary steps in the
:guilabel:`Configure Your Server` wizard, and then click
:guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Microsoft Exchange dialog box, click Apply and then click OK.

On the Choose Service page, select Microsoft Exchange or compatible service, and then click Next.

Read the preliminary steps in the Configure Your Server wizard, and then click Next.

</td>
</tr>
</table>Format using **boldface**.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
To access the web interface, open your web browser and
navigate to **http://yourDomain.com/zipit-install.php**.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
To access the web interface, open your web browser and navigate to **http://yourDomain.com/zipit-install.php**.

</td>
</tr>
</table>Links and Cross-References.

Format using **boldface**.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Server` text box, type **outlook**.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Server text box, type **outlook**.

</td>
</tr>
</table>Format inline text that the user types into an IDE, editor, or prompt using `monospace` text. Recommend using a `.. code-block::` instead.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Create a file by using a text editor. Insert the
following code: ``<?php phpinfo(); ?>``

For the username, enter ``admin``.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Create a file by using a text editor, and insert the following code: `<?php phpinfo(); ?>`

For the username, enter `admin`.

</td>
</tr>
</table>Placeholder or Variable Text.

Format using the `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
In the :guilabel:`Network Connections` window,
right-click the private adapter and select
:guilabel:`Properties`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
In the Network Connections window, right-click the private adapter and select Properties.

</td>
</tr>
</table>Format using the `:guilabel:` role.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
On the :guilabel:`Welcome` page of the :guilabel:`Active
Directory Domain Services Installation` Wizard, clear
the :guilabel:`Use advanced mode installation` check
box, and then click :guilabel:`Next`.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
On the Welcome page of the Active Directory Domain Services Installation Wizard, clear the Use advanced mode installation check box, and then click Next.

</td>
</tr>
</table>Format using *italics*.

<table>

<tr>
<td>
Code Example

</td>
<td>
```rst
Don't use *button* and *icon* interchangeably. If you're
referring to a command button or toolbar button (labeled
or unlabeled), use *button*. If you're referring to a
graphic on a screen, window, or other area, use *icon*.
```

</td>
</tr>
<tr>
<td>
Rendered Example

</td>
<td>
Don't use *button* and *icon* interchangeably. If you're referring to a command button or toolbar button (labeled or unlabeled), use *button*. If you're referring to a graphic on a screen, window, or other area, use *icon*.

</td>
</tr>
</table>
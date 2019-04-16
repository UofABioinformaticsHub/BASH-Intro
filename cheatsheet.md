# Cheatsheet for UofABioinformaticsHub Introduction to BASH Workshop




**Navigation and file management**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:----------- |:----------------------------- |:------------------ |:------------------ |
| `man`       | Display on-line manual        | `-k`                 |
| `pwd`       | Print working directory, i.e show where you are | none commonly used |
| `ls`        | List contents of a directory  | `-a`, `-h`, `-l`         |
| `cd`        | Change directory              | (scroll down in `man builtins` to find `cd`) |
| `mv`        |                               | `-b`, `-f`, `-u`         |
| `cp`        |                               | `-b`, `-f`, `-u`         |
| `rm`        |                               | `-r` (careful...)    |
| `rmdir`     |                               |                    |
| `mkdir`     |                               | `-p`                 |





**File viewing**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:----------- |:----------------------------- |:------------------ |:------------------ |
| `cat`       |                               |                    |
| `less`      |                               |                    |
| `more`      |                               |                    |
| `head`      |                               | `-n#` (e.g., `-n100`)  |
| `tail`      |                               | `-n#` (e.g., `-n100`)  |
| `wc`        |                               | `-l`                 |





**Keyboard shortcuts**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:----------- |:----------------------------- |:------------------ |:------------------ |
| [Tab]       | tab-autocomplete              |                    |                    |
| [Up]/[Down] | Cycle through previous commands |                    |
| [Ctrl][Shift]-C, [Ctrl][Shift]-V      | Copy and paste highlighted text in terminal |  |




**Filters, file/stream editing**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:----------- |:----------------------------- |:------------------ |:------------------ |
| `cut`       |                               | `-d`, `-f`, `-s`         |
| `paste`     |                               |                    |
| `sort`      |                               |                    |
| `uniq`      |                               | `-c`                 |
| `grep`      |                               |                    |
| `echo`      |                               | `-e`                 |
| `tee`       |                               |                    |
| `sed`       |                               |                    |
| `awk`       |                               |                    |


**General utilities**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:------------------ |:--------------- |:------------------ |:--------- |
| `history`          |                 | `-c`                 |           |
| `top`              |                 |                    |           |
| `ps`               |                 | `-u`                 |           |
| `kill`, `pkill`    |                 | `-u`                 |           |
| `whoami`           |                 | `-u`                 |           |
| `fg`               | bring process to foreground |        |           |


**Network**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:------------------ |:--------------- |:------------------ |:--------- |
| `wget`             |                 |                    |           |
| `curl`             |                 |                    |           |


**Special symbols**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:------------------ |:--------------- |:------------------ |:--------- |
| <code>&#124;</code> |                 |                    |           |
| `>`, `>>`          |                 |                    |           |
| `<`                |                 |                    |           |
| `&`                |                 |                    |           |
| `*`, `?`           | wildcards       |                    |           |
| `\`                |                 |                    |           |



**Archiving and compression**

| **Command/Symbol** | **Description** | **Useful options** |  Section  |
|:------------------ |:--------------- |:------------------ |:--------- |
| `tar`              |                 | `-x` `-z` `-c` `-v` `-f`     |           |
| `gunzip`, `gzip`   |                 | `-k`, `-c`             |           |


























<!--
<table>

<tr><td colspan="4" height=80><b>File system navigation and file management</b></td></tr>

<tr><th>Command/Symbol</th><th>Descrption</th><th>Useful options</th><th>Section</th>

<tr><td>`man`</td>
    <td>Display on-line manual</td>
    <td></td>
    <td></td>
</tr>
<tr><td>`pwd`</td>
    <td>Print working directory, i.e show where you are</td>
    <td>none commonly used</td>
    <td></td>
</tr>
<tr><td>`ls`</td>
    <td>List contents of a directory</td>
    <td>-a, -h, -l</td>
    <td></td>
</tr>
<tr><td>`cd`</td>
    <td>Change directory</td>
    <td></td>
    <td></td>
</tr>
<tr><td>`mv`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`cp`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`rm`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`rmdir`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`mkdir`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>

<tr><td colspan="4"></td> </tr>

<tr><td colspan="4" height=80>**File viewing**</td></tr>

<tr><th>Command/Symbol</th><th>Descrption</th><th>Useful options</th><th>Section</th>
<tr><td>`cat`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`more`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`less`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`head`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`tail`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`wc`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`grep`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>

<tr><td colspan="4"></td> </tr>


<tr><td colspan="4" height=80>**Keyboard Shortcuts**</td></tr>

<tr><th>Command/Symbol</th><th>Descrption</th><th>Useful options</th><th>Section</th>
<tr><td>[Tab] key</td>
    <td>Tab auto-complete</td>
    <td></td>
    <td></td>
</tr>
<tr><td>[Up]/[Down] arrow keys</td>
    <td>Cycle through previous commands</td>
    <td></td>
    <td></td>
</tr>
<tr><td>[Ctrl]+[Shift]+C, [Ctrl]+[Shift]+V</td>
    <td>Copy and paste highlighted text in terminal</td>
    <td></td>
    <td></td>
</tr>

<tr><td colspan="4"></td> </tr>
<tr><td colspan="4" height=80>**File/Stream editing**</td></tr>
<tr><th>Command/Symbol</th><th>Descrption</th><th>Useful options</th><th>Section</th>
<tr><td>`echo`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`sed`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`awk`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>

<tr><td colspan="4"></td> </tr>
<tr><td colspan="4" height=80>**Special characters/symbols**</td></tr>
<tr><th>Command/Symbol</th><th>Descrption</th><th>Useful options</th><th>Section</th>
<tr><td>`|`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`&`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`>`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr><td>`<`</td>
    <td></td>
    <td></td>
    <td></td>
</tr>


<tr><td colspan="4"></td> </tr>


<tr><td height=500 colspan="4"></td></tr>

</table> -->

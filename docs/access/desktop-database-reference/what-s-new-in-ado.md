---
title: Новые возможности в ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302613"
---
# <a name="whats-new-in-ado"></a>Что нового в ADO

**Область применения**: Access 2013, Office 2013 
 
Следующие новые функции и улучшенная документация включены в выпуск ADO 2.5. Этот список охватывает ADO, ADO MD и ADOX.

## <a name="new-features"></a>Новые функции

- **[Записи и потоки](chapter-10-records-and-streams.md)**

  В этом выпуске ADO представлен объект [Record,](record-object-ado.md) который может представлять такие объекты, как каталоги и файлы в файловой системе, а также папки и сообщения в почтовой системе и управлять ими. Запись **также** может представлять строку в наборе [записей,](recordset-object-ado.md)хотя объекты **Record** и **Recordset** имеют разные методы и свойства.

  Новый объект [Stream](stream-object-ado.md) предоставляет средства чтения, записи и управления двоичным потоком (в том или ином виде) или текстом, составляющим файл или поток сообщений.

- **[Использование URL-адресов](absolute-and-relative-urls.md)**

  В этом выпуске также вводится использование URL-адресов в качестве альтернативы строкам подключения и тексту команд для имен объектов хранения данных. URL-адреса могут использоваться с существующими объектами [Connection](connection-object-ado.md) и **Recordset,** а также с новыми объектами **Record** и **Stream.**

  В этом выпуске ADO поддерживает поставщиков OLE DB, которые распознают собственные схемы URL-адресов. Например, поставщик [OLE DB для](microsoft-ole-db-provider-for-internet-publishing.md)публикации в *Интернете,* который имеет доступ к файловой системе Windows 2000, распознает существующую схему HTTP.

- **[Специальные поля для поставщиков источников документов](records-and-provider-supplied-fields.md)**

  Особый класс поставщиков, называемых *поставщиками* источников документов, управляет папками и документами. Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источника документов заполняет эти объекты уникальным набором полей, описывая характеристики документа. Эти поля представляют собой *запись ресурса*  или **набор записей.**

## <a name="new-reference-topics"></a>Новые справочные разделы

### <a name="properties"></a>Свойства

В этот выпуск включены следующие новые свойства.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Свойство</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Charset</a></p></td>
<td><p>Указывает набор символов, в который необходимо перевести содержимое текстового объекта <strong>Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Указывает, находится ли текущая позиция в конце потока.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Указывает двоичный символ, который будет использоваться в качестве разных строк в текстовых <strong>объектах Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Указывает доступные разрешения на изменение данных в объекте <strong>Connection,</strong> <strong>Record</strong>или <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Указывает абсолютную строку URL-адреса, которая указывает на родительская <strong>запись</strong> текущего объекта <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Указывает текущее положение в <strong>объекте Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Указывает тип объекта <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Размер</a></p></td>
<td><p>Указывает размер потока в количестве в 100 000 000 000 000 000 000 000 00</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Указывает сущность, представленную объектом <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Указывает на все применимые объекты, независимо от того, является ли состояние объекта открытым или закрытым. Указывает для всех применимых объектов, которые выполняют асинхронный метод, независимо от того, подключается ли, выполняется или выполняется текущий объект.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Тип</a></p></td>
<td><p>Указывает тип данных, содержащихся в объекте <strong>Stream</strong> (двоичный или текстовый).</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Methods

В этот выпуск включены следующие новые методы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Копирует файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Копирует указанное количество символов или ветвей (в зависимости от <strong>типа)</strong>в <strong>объекте Stream</strong> <strong></strong> в другой <strong>объект Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Удаляет файл или каталог и все его подкадиректоры.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Flush</a></p></td>
<td><p>Привнося содержимое объекта <strong>Stream,</strong> оставшегося в буфере ADO, к основному объекту, с которым связан объект <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Возвращает набор <strong>записей,</strong> строки которого представляют файлы и подкадиректоры в каталоге, представленном этой <strong>записью.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Загружает содержимое существующего файла в объект <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Перемещает файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Открывает существующий <strong>объект Record</strong> или создает новый файл или каталог.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Считывает указанное количество ветвей из двоичного объекта <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Считывая указанное количество символов из объекта <strong>Text Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Сохраняет двоичное содержимое <strong>Stream</strong> в файл.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Задает положение, которое является окончанием потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Пропускает всю строку при чтении объекта <strong>Text Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Записывает двоичные данные в <strong>объект Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Записывает указанную текстовую строку в <strong>объект Stream.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Новая и улучшенная документация

- **[Примеры кода](ado-code-examples.md)**

  Примеры были расширены и содержат примеры кода, написанные на Microsoft Visual C++ и Microsoft Visual J++. Эти примеры кода можно скопировать и вкопировать в редактор.

- **[Разделы о поставщиках](appendix-a-providers.md)**

  Включен новый раздел, поясняется, как использовать ADO с [поставщиком OLE DB для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)

- **[Программирование с помощью ADO](appendix-c-programming-with-ado.md)**

  В этом новом разделе содержатся советы и рекомендации по использованию ADO с различными языками программирования. Он содержит существующие индексы синтаксиса для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения для разработчиков, использующих Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ или Microsoft Visual J++.


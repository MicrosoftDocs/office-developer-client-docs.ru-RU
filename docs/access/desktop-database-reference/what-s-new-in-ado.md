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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713634"
---
# <a name="whats-new-in-ado"></a>Что нового в ADO

**Применимо к**: Access 2013, Office 2013 
 
В ADO 2.5 включены следующие новые функции и улучшенные документации выпуска системы. Этот список содержит ADO, ADO MD и ADOX.

## <a name="new-features"></a>Новые возможности

- **[Записей и потоков](chapter-10-records-and-streams.md)**

  В этом выпуске ADO представляется объекта [записи](record-object-ado.md) , которое можно представления и управления каталоги и файлы в файловой системе и папки и сообщения в системы электронной почты. **Запись** также может представлять строки в наборе [записей](recordset-object-ado.md), несмотря на то, что **запись** и **набора записей** объекты имеют различные методы и свойства.

  Новый объект [потока](stream-object-ado.md) предоставляет средства для чтения, записи и управление двоичный поток байт или текст, образующих потока файл или сообщение.

- **[Об использовании URL-адреса](absolute-and-relative-urls.md)**

  В этом выпуске также включает использование указатели универсальный код ресурса (URL-адреса), в качестве альтернативы для строки подключения и текст команды, имен объектов хранилища данных. URL-адреса могут быть использованы с помощью существующего [подключения](connection-object-ado.md) и объектов **наборов записей** , а также новые объекты **потока** и **записи** .

  В этом выпуске ADO поддерживает поставщики OLE DB, распознает собственные схемы URL-адрес. Например, [Поставщик OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)*,* которого получает доступ к файловой системе Windows 2000, распознает существующую схему HTTP.

- **[Особых полей для поставщиков исходного документа](records-and-provider-supplied-fields.md)**

  Специальный класс поставщиков, называется поставщики *источников документов* , управление папки и документы. Когда объект **записи** представляет документ, или объекта **набора записей** представляет папку документов, поставщик источника документов заполняет объектам с уникальный набор полей, описывающих характеристики документа. Эти поля составляют *ресурсов* **записи** или **набора записей**.

## <a name="new-reference-topics"></a>Новые разделы справочника по

### <a name="properties"></a>Свойства

В этой версии включены следующие новые свойства.

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
<td><p><a href="charset-property-ado.md">Набор символов</a></p></td>
<td><p>Указывает кодировку, в которой содержимое объект текстового <strong>потока</strong> преобразования.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Указывает, является ли текущую позицию в конце потока.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Указывает двоичных символов для использования в качестве разделителя строки в объектах <strong>потока</strong> текста.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Указывает, доступные права на изменение данных в объекте <strong>подключения</strong>, <strong>запись</strong>или <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Указывает строку абсолютный URL-адрес, указывающий на родительской <strong>записи</strong> текущего объекта <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Указывает текущую позицию в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Указывает тип объекта <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></p></td>
<td><p>Указывает размер потока в байтах.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Указывает сущности, представленного объектом <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой. Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Type</a></p></td>
<td><p>Указывает тип данных, содержащихся в объект <strong>Stream</strong> (двоичный или текст).</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Методы

В этой версии включены следующие новые методы.

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
<td><p>Копирует указанного числа символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> <strong>объекта</strong> в другой объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Удаляет файл или каталог и все его подкаталоги.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Очистка</a></p></td>
<td><p>Принудительно содержимое на объект <strong>Stream</strong> , оставшихся в буфер ADO для базового объекта, с которым связан объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Возвращает <strong>набор записей</strong> , строки представляют файлы и вложенные папки в каталоге, представленный этим <strong>запись.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Загружает содержимое существующего файла в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Перемещает файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Открывает существующий объект <strong>записи</strong> или создает новый файл или каталог.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Открывает объект <strong>Stream</strong> для работы с потоки данных двоичный или текст.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Считывает указанное число байтов из двоичного объекта <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Число операций чтения указанное число символов из объекта <strong>потока</strong> текста.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Сохраняет двоичные содержимое <strong>потока</strong> в файл.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Задает позицию за конец потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Пропускает одну всю строку при чтении объект текстового <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Записывает двоичные данные в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Записывает строку, указанный текст в объект <strong>потока</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Новые и усовершенствованные документации

- **[Разделы с примерами кода](ado-code-examples.md)**

  Примеры дополнены и содержит примеры кода, записанные в Microsoft Visual C++ и Microsoft Visual J ++. Можно скопировать и вставить этих примеров кода в редактора.

- **[Разделы поставщика](appendix-a-providers.md)**

  Новый раздел включен, сведения об использовании ADO с помощью [Поставщика OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).

- **[Программирование с использованием ADO](appendix-c-programming-with-ado.md)**

  Этот новый раздел содержит советы и рекомендации по использованию ADO на различных языках программирования. Он содержит существующие индексы синтаксис для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения, относящиеся к разработчиков (en) с помощью Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, или Microsoft Visual J ++.


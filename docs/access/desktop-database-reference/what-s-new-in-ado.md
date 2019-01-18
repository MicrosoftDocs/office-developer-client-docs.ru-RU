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
# <a name="whats-new-in-ado"></a><span data-ttu-id="5cda9-102">Что нового в ADO</span><span class="sxs-lookup"><span data-stu-id="5cda9-102">What's new in ADO</span></span>

<span data-ttu-id="5cda9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cda9-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="5cda9-104">В ADO 2.5 включены следующие новые функции и улучшенные документации выпуска системы.</span><span class="sxs-lookup"><span data-stu-id="5cda9-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="5cda9-105">Этот список содержит ADO, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="5cda9-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="5cda9-106">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="5cda9-106">New features</span></span>

- <span data-ttu-id="5cda9-107">**[Записей и потоков](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="5cda9-108">В этом выпуске ADO представляется объекта [записи](record-object-ado.md) , которое можно представления и управления каталоги и файлы в файловой системе и папки и сообщения в системы электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5cda9-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="5cda9-109">**Запись** также может представлять строки в наборе [записей](recordset-object-ado.md), несмотря на то, что **запись** и **набора записей** объекты имеют различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="5cda9-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="5cda9-110">Новый объект [потока](stream-object-ado.md) предоставляет средства для чтения, записи и управление двоичный поток байт или текст, образующих потока файл или сообщение.</span><span class="sxs-lookup"><span data-stu-id="5cda9-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="5cda9-111">**[Об использовании URL-адреса](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="5cda9-112">В этом выпуске также включает использование указатели универсальный код ресурса (URL-адреса), в качестве альтернативы для строки подключения и текст команды, имен объектов хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="5cda9-112">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects.</span></span> <span data-ttu-id="5cda9-113">URL-адреса могут быть использованы с помощью существующего [подключения](connection-object-ado.md) и объектов **наборов записей** , а также новые объекты **потока** и **записи** .</span><span class="sxs-lookup"><span data-stu-id="5cda9-113">URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="5cda9-114">В этом выпуске ADO поддерживает поставщики OLE DB, распознает собственные схемы URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5cda9-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="5cda9-115">Например, [Поставщик OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)*,* которого получает доступ к файловой системе Windows 2000, распознает существующую схему HTTP.</span><span class="sxs-lookup"><span data-stu-id="5cda9-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="5cda9-116">**[Особых полей для поставщиков исходного документа](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="5cda9-117">Специальный класс поставщиков, называется поставщики *источников документов* , управление папки и документы.</span><span class="sxs-lookup"><span data-stu-id="5cda9-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="5cda9-118">Когда объект **записи** представляет документ, или объекта **набора записей** представляет папку документов, поставщик источника документов заполняет объектам с уникальный набор полей, описывающих характеристики документа.</span><span class="sxs-lookup"><span data-stu-id="5cda9-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="5cda9-119">Эти поля составляют *ресурсов* **записи** или **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5cda9-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="5cda9-120">Новые разделы справочника по</span><span class="sxs-lookup"><span data-stu-id="5cda9-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="5cda9-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cda9-121">Properties</span></span>

<span data-ttu-id="5cda9-122">В этой версии включены следующие новые свойства.</span><span class="sxs-lookup"><span data-stu-id="5cda9-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cda9-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="5cda9-123">Property</span></span></p></th>
<th><p><span data-ttu-id="5cda9-124">Описание</span><span class="sxs-lookup"><span data-stu-id="5cda9-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-125"><a href="charset-property-ado.md">Набор символов</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-126">Указывает кодировку, в которой содержимое объект текстового <strong>потока</strong> преобразования.</span><span class="sxs-lookup"><span data-stu-id="5cda9-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-128">Указывает, является ли текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="5cda9-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-130">Указывает двоичных символов для использования в качестве разделителя строки в объектах <strong>потока</strong> текста.</span><span class="sxs-lookup"><span data-stu-id="5cda9-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-132">Указывает, доступные права на изменение данных в объекте <strong>подключения</strong>, <strong>запись</strong>или <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-134">Указывает строку абсолютный URL-адрес, указывающий на родительской <strong>записи</strong> текущего объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-136">Указывает текущую позицию в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-138">Указывает тип объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-140">Указывает размер потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="5cda9-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-142">Указывает сущности, представленного объектом <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-144">Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.</span><span class="sxs-lookup"><span data-stu-id="5cda9-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="5cda9-145">Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="5cda9-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-146"><a href="type-property-ado-stream.md">Type</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-147">Указывает тип данных, содержащихся в объект <strong>Stream</strong> (двоичный или текст).</span><span class="sxs-lookup"><span data-stu-id="5cda9-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="5cda9-148">Методы</span><span class="sxs-lookup"><span data-stu-id="5cda9-148">Methods</span></span>

<span data-ttu-id="5cda9-149">В этой версии включены следующие новые методы.</span><span class="sxs-lookup"><span data-stu-id="5cda9-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cda9-150">Метод</span><span class="sxs-lookup"><span data-stu-id="5cda9-150">Method</span></span></p></th>
<th><p><span data-ttu-id="5cda9-151">Описание</span><span class="sxs-lookup"><span data-stu-id="5cda9-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-153">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="5cda9-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-155">Копирует указанного числа символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> <strong>объекта</strong> в другой объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-157">Удаляет файл или каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="5cda9-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-158"><a href="flush-method-ado.md">Очистка</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-159">Принудительно содержимое на объект <strong>Stream</strong> , оставшихся в буфер ADO для базового объекта, с которым связан объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-161">Возвращает <strong>набор записей</strong> , строки представляют файлы и вложенные папки в каталоге, представленный этим <strong>запись.</strong></span><span class="sxs-lookup"><span data-stu-id="5cda9-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-163">Загружает содержимое существующего файла в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-165">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="5cda9-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-167">Открывает существующий объект <strong>записи</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="5cda9-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-169">Открывает объект <strong>Stream</strong> для работы с потоки данных двоичный или текст.</span><span class="sxs-lookup"><span data-stu-id="5cda9-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-171">Считывает указанное число байтов из двоичного объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-173">Число операций чтения указанное число символов из объекта <strong>потока</strong> текста.</span><span class="sxs-lookup"><span data-stu-id="5cda9-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-175">Сохраняет двоичные содержимое <strong>потока</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="5cda9-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-177">Задает позицию за конец потока.</span><span class="sxs-lookup"><span data-stu-id="5cda9-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-179">Пропускает одну всю строку при чтении объект текстового <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cda9-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-181">Записывает двоичные данные в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cda9-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="5cda9-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="5cda9-183">Записывает строку, указанный текст в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cda9-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="5cda9-184">Новые и усовершенствованные документации</span><span class="sxs-lookup"><span data-stu-id="5cda9-184">New and enhanced documentation</span></span>

- <span data-ttu-id="5cda9-185">**[Разделы с примерами кода](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="5cda9-186">Примеры дополнены и содержит примеры кода, записанные в Microsoft Visual C++ и Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="5cda9-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="5cda9-187">Можно скопировать и вставить этих примеров кода в редактора.</span><span class="sxs-lookup"><span data-stu-id="5cda9-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="5cda9-188">**[Разделы поставщика](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="5cda9-189">Новый раздел включен, сведения об использовании ADO с помощью [Поставщика OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="5cda9-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="5cda9-190">**[Программирование с использованием ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="5cda9-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="5cda9-191">Этот новый раздел содержит советы и рекомендации по использованию ADO на различных языках программирования.</span><span class="sxs-lookup"><span data-stu-id="5cda9-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="5cda9-192">Он содержит существующие индексы синтаксис для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения, относящиеся к разработчиков (en) с помощью Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, или Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="5cda9-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>


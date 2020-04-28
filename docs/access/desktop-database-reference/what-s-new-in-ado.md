---
title: Новые возможности объектов данных ActiveX (ADO)
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
# <a name="whats-new-in-ado"></a><span data-ttu-id="298c8-102">Что нового в ADO</span><span class="sxs-lookup"><span data-stu-id="298c8-102">What's new in ADO</span></span>

<span data-ttu-id="298c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="298c8-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="298c8-104">В выпуске ADO 2,5 включены следующие новые функции и расширенная документация.</span><span class="sxs-lookup"><span data-stu-id="298c8-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="298c8-105">В этом списке рассматриваются ADO, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="298c8-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="298c8-106">Новые функции</span><span class="sxs-lookup"><span data-stu-id="298c8-106">New features</span></span>

- <span data-ttu-id="298c8-107">**[Записи и потоки](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="298c8-108">В этом выпуске ADO представлен объект [Record](record-object-ado.md) , который может представлять и управлять такими объектами, как каталоги и файлы в файловой системе, а также папками и сообщениями в системе электронной почты.</span><span class="sxs-lookup"><span data-stu-id="298c8-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="298c8-109">**Запись** также может представлять собой строку в [наборе записей](recordset-object-ado.md), хотя объекты **записей** и **наборов записей** имеют различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="298c8-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="298c8-110">Новый объект [Stream](stream-object-ado.md) предоставляет средства для чтения, записи и управления двоичным потоком байтов или текстом, составляющим поток файла или сообщения.</span><span class="sxs-lookup"><span data-stu-id="298c8-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="298c8-111">**[Использование URL-адресов](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="298c8-112">В этом выпуске также представлено использование URL-адресов, в качестве альтернативы строке подключения и тексту команды, для именования объектов хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="298c8-112">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects.</span></span> <span data-ttu-id="298c8-113">URL-адреса можно использовать с существующими объектами [Connection](connection-object-ado.md) и **Recordset** , а также с новыми объектами **Record** и **Stream** .</span><span class="sxs-lookup"><span data-stu-id="298c8-113">URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="298c8-114">В этом выпуске ADO поддерживает поставщиков OLE DB, распознающих собственные схемы URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="298c8-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="298c8-115">Например, [поставщик OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md)*,* который получает доступ к файловой системе Windows 2000, распознает существующую схему HTTP.</span><span class="sxs-lookup"><span data-stu-id="298c8-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="298c8-116">**[Специальные поля для поставщиков источника документов](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="298c8-117">Особый класс поставщиков, называемый поставщиками *источников документов* , Управление папками и документами.</span><span class="sxs-lookup"><span data-stu-id="298c8-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="298c8-118">Когда объект **Record** представляет документ, или объект **Recordset** представляет папку документов, поставщик источника документа заполняет эти объекты уникальным набором полей, описывающих характеристики документа.</span><span class="sxs-lookup"><span data-stu-id="298c8-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="298c8-119">Эти поля составляют запись *ресурса* **Record** или **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="298c8-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="298c8-120">Новые справочные разделы</span><span class="sxs-lookup"><span data-stu-id="298c8-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="298c8-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="298c8-121">Properties</span></span>

<span data-ttu-id="298c8-122">В этот выпуск включены следующие новые свойства.</span><span class="sxs-lookup"><span data-stu-id="298c8-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298c8-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="298c8-123">Property</span></span></p></th>
<th><p><span data-ttu-id="298c8-124">Описание</span><span class="sxs-lookup"><span data-stu-id="298c8-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298c8-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="298c8-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-126">Указывает набор символов, в который необходимо перевести содержимое текстового объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="298c8-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-128">Указывает, находится ли текущая позиция в конце потока.</span><span class="sxs-lookup"><span data-stu-id="298c8-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="298c8-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-130">Указывает двоичный символ, который будет использоваться в качестве разделителя строк в текстовых объектах <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="298c8-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-132">Указывает доступные разрешения для изменения данных в объекте <strong>подключения</strong>, <strong>записи</strong>или <strong>потоке</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="298c8-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-134">Указывает строку абсолютного URL-адреса, указывающую на родительскую <strong>запись</strong> текущего объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="298c8-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-136">Указывает текущее положение в объекте <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="298c8-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-138">Указывает тип объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Размер</a></span><span class="sxs-lookup"><span data-stu-id="298c8-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-140">Указывает размер потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="298c8-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="298c8-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-142">Указывает сущность, представленную объектом <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="298c8-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-144">Указывает для всех применяемых объектов, независимо от того, является ли состояние объекта открытым или закрытым.</span><span class="sxs-lookup"><span data-stu-id="298c8-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="298c8-145">Указывает на то, что все применяемые объекты выполняют асинхронный метод, независимо от того, является ли текущее состояние объекта подключением, выполнением или извлечением.</span><span class="sxs-lookup"><span data-stu-id="298c8-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-146"><a href="type-property-ado-stream.md">Тип</a></span><span class="sxs-lookup"><span data-stu-id="298c8-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-147">Указывает тип данных, которые хранятся в объекте <strong>Stream</strong> (двоичный или текстовый).</span><span class="sxs-lookup"><span data-stu-id="298c8-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="298c8-148">Methods</span><span class="sxs-lookup"><span data-stu-id="298c8-148">Methods</span></span>

<span data-ttu-id="298c8-149">В этот выпуск включены следующие новые методы.</span><span class="sxs-lookup"><span data-stu-id="298c8-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298c8-150">Метод</span><span class="sxs-lookup"><span data-stu-id="298c8-150">Method</span></span></p></th>
<th><p><span data-ttu-id="298c8-151">Описание</span><span class="sxs-lookup"><span data-stu-id="298c8-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298c8-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="298c8-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-153">Копирует файл или каталог, а также его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="298c8-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="298c8-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-155">Копирует указанное число символов или байтов (в зависимости от <strong>типа</strong>) в <strong>объекте</strong> <strong>Stream</strong> в другой объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="298c8-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-157">Удаляет файл или каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="298c8-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-158"><a href="flush-method-ado.md">Удален</a></span><span class="sxs-lookup"><span data-stu-id="298c8-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-159">Принудительно применяет содержимое объекта <strong>Stream</strong> в буфере ADO к базовому объекту, с которым связан объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="298c8-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-161">Возвращает объект <strong>Recordset</strong> , строки которого представляют файлы и подкаталоги в каталоге, представленном этой <strong>записью.</strong></span><span class="sxs-lookup"><span data-stu-id="298c8-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="298c8-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-163">Загружает содержимое существующего файла в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="298c8-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-165">Перемещает файл или каталог вместе с его содержимым в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="298c8-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="298c8-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-167">Открывает существующий объект <strong>Record</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="298c8-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="298c8-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-169">Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="298c8-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-170"><a href="read-method-ado.md">Чтение</a></span><span class="sxs-lookup"><span data-stu-id="298c8-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-171">Считывает указанное число байтов из двоичного объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="298c8-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-173">Считывает указанное число символов из текстового объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="298c8-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-175">Сохраняет двоичное содержимое <strong>потока</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="298c8-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="298c8-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-177">Задает позицию, которая является концом потока.</span><span class="sxs-lookup"><span data-stu-id="298c8-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="298c8-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-179">Пропускает одну строку целиком при чтении объекта текстового <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298c8-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="298c8-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-181">Записывает двоичные данные в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298c8-182"><a href="writetext-method-ado.md">Инструкция</a></span><span class="sxs-lookup"><span data-stu-id="298c8-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="298c8-183">Записывает указанную текстовую строку в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="298c8-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="298c8-184">Новая и расширенная документация</span><span class="sxs-lookup"><span data-stu-id="298c8-184">New and enhanced documentation</span></span>

- <span data-ttu-id="298c8-185">**[Разделы с примерами кода](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="298c8-186">Примеры были расширены, чтобы содержать примеры кода, написанные в Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="298c8-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="298c8-187">Вы можете скопировать и вставить эти примеры кода в свой редактор.</span><span class="sxs-lookup"><span data-stu-id="298c8-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="298c8-188">**[Разделы поставщика](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="298c8-189">В этой статье описано, как использовать ADO с [поставщиком OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="298c8-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="298c8-190">**[Программирование с использованием ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="298c8-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="298c8-191">В этом новом разделе содержатся советы и рекомендации по использованию ADO с различными языками программирования.</span><span class="sxs-lookup"><span data-stu-id="298c8-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="298c8-192">Он содержит существующие индексы синтаксиса для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения, характерные для разработчиков, использующих Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ или Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="298c8-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>


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
# <a name="whats-new-in-ado"></a><span data-ttu-id="2d3d7-102">Что нового в ADO</span><span class="sxs-lookup"><span data-stu-id="2d3d7-102">What's new in ADO</span></span>

<span data-ttu-id="2d3d7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d3d7-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="2d3d7-104">Следующие новые функции и улучшенная документация включены в выпуск ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="2d3d7-105">Этот список охватывает ADO, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="2d3d7-106">Новые функции</span><span class="sxs-lookup"><span data-stu-id="2d3d7-106">New features</span></span>

- <span data-ttu-id="2d3d7-107">**[Записи и потоки](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="2d3d7-108">В этом выпуске ADO представлен объект [Record,](record-object-ado.md) который может представлять такие объекты, как каталоги и файлы в файловой системе, а также папки и сообщения в почтовой системе и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="2d3d7-109">Запись **также** может представлять строку в наборе [записей,](recordset-object-ado.md)хотя объекты **Record** и **Recordset** имеют разные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="2d3d7-110">Новый объект [Stream](stream-object-ado.md) предоставляет средства чтения, записи и управления двоичным потоком (в том или ином виде) или текстом, составляющим файл или поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="2d3d7-111">**[Использование URL-адресов](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="2d3d7-112">В этом выпуске также вводится использование URL-адресов в качестве альтернативы строкам подключения и тексту команд для имен объектов хранения данных.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-112">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects.</span></span> <span data-ttu-id="2d3d7-113">URL-адреса могут использоваться с существующими объектами [Connection](connection-object-ado.md) и **Recordset,** а также с новыми объектами **Record** и **Stream.**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-113">URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="2d3d7-114">В этом выпуске ADO поддерживает поставщиков OLE DB, которые распознают собственные схемы URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="2d3d7-115">Например, поставщик [OLE DB для](microsoft-ole-db-provider-for-internet-publishing.md)публикации в *Интернете,* который имеет доступ к файловой системе Windows 2000, распознает существующую схему HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="2d3d7-116">**[Специальные поля для поставщиков источников документов](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="2d3d7-117">Особый класс поставщиков, называемых *поставщиками* источников документов, управляет папками и документами.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="2d3d7-118">Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источника документов заполняет эти объекты уникальным набором полей, описывая характеристики документа.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="2d3d7-119">Эти поля представляют собой *запись ресурса*  или **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="2d3d7-120">Новые справочные разделы</span><span class="sxs-lookup"><span data-stu-id="2d3d7-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="2d3d7-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d3d7-121">Properties</span></span>

<span data-ttu-id="2d3d7-122">В этот выпуск включены следующие новые свойства.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d3d7-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d3d7-123">Property</span></span></p></th>
<th><p><span data-ttu-id="2d3d7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2d3d7-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-126">Указывает набор символов, в который необходимо перевести содержимое текстового объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-128">Указывает, находится ли текущая позиция в конце потока.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-130">Указывает двоичный символ, который будет использоваться в качестве разных строк в текстовых <strong>объектах Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-132">Указывает доступные разрешения на изменение данных в объекте <strong>Connection,</strong> <strong>Record</strong>или <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-134">Указывает абсолютную строку URL-адреса, которая указывает на родительская <strong>запись</strong> текущего объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-136">Указывает текущее положение в <strong>объекте Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-138">Указывает тип объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Размер</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-140">Указывает размер потока в количестве в 100 000 000 000 000 000 000 000 00</span><span class="sxs-lookup"><span data-stu-id="2d3d7-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-142">Указывает сущность, представленную объектом <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-144">Указывает на все применимые объекты, независимо от того, является ли состояние объекта открытым или закрытым.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="2d3d7-145">Указывает для всех применимых объектов, которые выполняют асинхронный метод, независимо от того, подключается ли, выполняется или выполняется текущий объект.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-146"><a href="type-property-ado-stream.md">Тип</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-147">Указывает тип данных, содержащихся в объекте <strong>Stream</strong> (двоичный или текстовый).</span><span class="sxs-lookup"><span data-stu-id="2d3d7-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="2d3d7-148">Methods</span><span class="sxs-lookup"><span data-stu-id="2d3d7-148">Methods</span></span>

<span data-ttu-id="2d3d7-149">В этот выпуск включены следующие новые методы.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d3d7-150">Метод</span><span class="sxs-lookup"><span data-stu-id="2d3d7-150">Method</span></span></p></th>
<th><p><span data-ttu-id="2d3d7-151">Описание</span><span class="sxs-lookup"><span data-stu-id="2d3d7-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-153">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-155">Копирует указанное количество символов или ветвей (в зависимости от <strong>типа)</strong>в <strong>объекте Stream</strong> <strong></strong> в другой <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-157">Удаляет файл или каталог и все его подкадиректоры.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-158"><a href="flush-method-ado.md">Flush</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-159">Привнося содержимое объекта <strong>Stream,</strong> оставшегося в буфере ADO, к основному объекту, с которым связан объект <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-161">Возвращает набор <strong>записей,</strong> строки которого представляют файлы и подкадиректоры в каталоге, представленном этой <strong>записью.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-163">Загружает содержимое существующего файла в объект <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-165">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-167">Открывает существующий <strong>объект Record</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-169">Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-171">Считывает указанное количество ветвей из двоичного объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-173">Считывая указанное количество символов из объекта <strong>Text Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-175">Сохраняет двоичное содержимое <strong>Stream</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-177">Задает положение, которое является окончанием потока.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-179">Пропускает всю строку при чтении объекта <strong>Text Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d3d7-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-181">Записывает двоичные данные в <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d3d7-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="2d3d7-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="2d3d7-183">Записывает указанную текстовую строку в <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="2d3d7-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="2d3d7-184">Новая и улучшенная документация</span><span class="sxs-lookup"><span data-stu-id="2d3d7-184">New and enhanced documentation</span></span>

- <span data-ttu-id="2d3d7-185">**[Примеры кода](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="2d3d7-186">Примеры были расширены и содержат примеры кода, написанные на Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="2d3d7-187">Эти примеры кода можно скопировать и вкопировать в редактор.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="2d3d7-188">**[Разделы о поставщиках](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="2d3d7-189">Включен новый раздел, поясняется, как использовать ADO с [поставщиком OLE DB для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="2d3d7-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="2d3d7-190">**[Программирование с помощью ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="2d3d7-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="2d3d7-191">В этом новом разделе содержатся советы и рекомендации по использованию ADO с различными языками программирования.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="2d3d7-192">Он содержит существующие индексы синтаксиса для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения для разработчиков, использующих Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ или Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="2d3d7-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>


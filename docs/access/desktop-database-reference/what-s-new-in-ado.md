---
title: Что нового в ActiveX объектах данных (ADO)
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
# <a name="whats-new-in-ado"></a><span data-ttu-id="d0398-102">Что нового в ADO</span><span class="sxs-lookup"><span data-stu-id="d0398-102">What's new in ADO</span></span>

<span data-ttu-id="d0398-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0398-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="d0398-104">Следующие новые функции и расширенная документация включены в выпуск ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="d0398-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="d0398-105">Этот список охватывает ADO, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="d0398-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="d0398-106">Новые функции</span><span class="sxs-lookup"><span data-stu-id="d0398-106">New features</span></span>

- <span data-ttu-id="d0398-107">**[Записи и потоки](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="d0398-108">В этом выпуске ADO представлен объект [Record,](record-object-ado.md) который может представлять и управлять вещами, например каталогами и файлами в файловой системе, а также папками и сообщениями в системе электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d0398-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="d0398-109">Запись **также** может представлять строку в [наборе Recordset,](recordset-object-ado.md)хотя объекты **Record** и **Recordset** имеют различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="d0398-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="d0398-110">Новый объект [Stream](stream-object-ado.md) предоставляет средства для чтения, записи и управления двоичным потоком bytes или текста, которые включают файл или поток сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0398-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="d0398-111">**[Использование URL-адреса](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="d0398-112">В этом выпуске также вводится использование единообразных локаторов ресурсов (URL-адресов) в качестве альтернативы строкам подключения и тексту команд, чтобы назвать объекты хранения данных.</span><span class="sxs-lookup"><span data-stu-id="d0398-112">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects.</span></span> <span data-ttu-id="d0398-113">URL-адреса можно использовать с существующими объектами [Подключения](connection-object-ado.md) и **Recordset,** а также с новыми объектами **Record** и **Stream.**</span><span class="sxs-lookup"><span data-stu-id="d0398-113">URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="d0398-114">В этом выпуске ADO поддерживает поставщиков OLE DB, которые распознают собственные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="d0398-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="d0398-115">Например, [поставщик OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)для интернет-публикации, который имеет доступ к файловой системе Windows 2000, распознает существующую схему HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0398-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="d0398-116">**[Специальные поля для поставщиков источников документов](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="d0398-117">Особый класс поставщиков, называемых *поставщиками* источников документов, управляет папками и документами.</span><span class="sxs-lookup"><span data-stu-id="d0398-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="d0398-118">Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источников документов заполняет эти объекты уникальным набором полей, описывая характеристики документа.</span><span class="sxs-lookup"><span data-stu-id="d0398-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="d0398-119">Эти поля представляют собой *ресурс* **Record** или **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d0398-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="d0398-120">Новые справочные темы</span><span class="sxs-lookup"><span data-stu-id="d0398-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="d0398-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0398-121">Properties</span></span>

<span data-ttu-id="d0398-122">В этот выпуск включены следующие новые свойства.</span><span class="sxs-lookup"><span data-stu-id="d0398-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0398-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="d0398-123">Property</span></span></p></th>
<th><p><span data-ttu-id="d0398-124">Описание</span><span class="sxs-lookup"><span data-stu-id="d0398-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0398-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="d0398-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-126">Указывает набор символов, в который должно быть переведено содержимое объекта <strong>text Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="d0398-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-128">Указывает, находится ли текущая позиция в конце потока.</span><span class="sxs-lookup"><span data-stu-id="d0398-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="d0398-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-130">Указывает двоичный символ, который будет использоваться в качестве сепаратора строки в текстовых <strong>объектах Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="d0398-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-132">Указывает доступные разрешения на изменение данных в <strong>объекте Подключение,</strong> <strong>Запись</strong>или <strong>Поток.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="d0398-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-134">Указывает абсолютную строку URL-адреса, которая указывает на родительную <strong>запись</strong> текущего объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="d0398-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-136">Указывает текущее положение в <strong>объекте Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="d0398-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-138">Указывает тип объекта <strong>Запись.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Размер</a></span><span class="sxs-lookup"><span data-stu-id="d0398-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-140">Указывает размер потока в количестве bytes.</span><span class="sxs-lookup"><span data-stu-id="d0398-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="d0398-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-142">Указывает сущность, представленную объектом <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-143"><a href="state-property-ado.md">Состояние</a></span><span class="sxs-lookup"><span data-stu-id="d0398-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-144">Указывает для всех применимых объектов, открытое или закрытое состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d0398-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="d0398-145">Указывает для всех применимых объектов, исполняющих асинхронный метод, независимо от того, подключен ли текущий объект, выполняется или выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0398-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-146"><a href="type-property-ado-stream.md">Тип</a></span><span class="sxs-lookup"><span data-stu-id="d0398-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-147">Указывает тип данных, содержащихся в <strong>объекте Stream</strong> (двоичный или текстовый).</span><span class="sxs-lookup"><span data-stu-id="d0398-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="d0398-148">Методы</span><span class="sxs-lookup"><span data-stu-id="d0398-148">Methods</span></span>

<span data-ttu-id="d0398-149">В этот выпуск включены следующие новые методы.</span><span class="sxs-lookup"><span data-stu-id="d0398-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0398-150">Метод</span><span class="sxs-lookup"><span data-stu-id="d0398-150">Method</span></span></p></th>
<th><p><span data-ttu-id="d0398-151">Описание</span><span class="sxs-lookup"><span data-stu-id="d0398-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0398-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="d0398-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-153">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="d0398-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="d0398-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-155">Копирует указанное количество символов или bytes (в зависимости от <strong>типа)</strong>в <strong>объекте Stream</strong> <strong>на</strong> другой объект <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="d0398-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-157">Удаляет файл или каталог и все его подтеки.</span><span class="sxs-lookup"><span data-stu-id="d0398-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-158"><a href="flush-method-ado.md">Флеш</a></span><span class="sxs-lookup"><span data-stu-id="d0398-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-159">Привнося содержимое объекта <strong>Stream,</strong> оставшегося в буфере ADO, к основному объекту, с которым связан объект <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="d0398-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-161">Возвращает набор <strong>записей,</strong> строки которого представляют файлы и подтеки в каталоге, представленном этой <strong>записью.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="d0398-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-163">Загружает содержимое существующего файла в объект <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="d0398-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-165">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="d0398-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="d0398-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-167">Открывает <strong>существующий объект Record</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="d0398-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="d0398-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-169">Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="d0398-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="d0398-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-171">Считывает определенное количество bytes из двоичного объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="d0398-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-173">Читает указанное количество символов из объекта text <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="d0398-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-175">Сохраняет двоичное содержимое <strong>потока в</strong> файл.</span><span class="sxs-lookup"><span data-stu-id="d0398-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="d0398-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-177">Задает позицию, которая является конечным потоком.</span><span class="sxs-lookup"><span data-stu-id="d0398-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="d0398-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-179">Пропускает всю строку при чтении объекта <strong>text Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0398-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="d0398-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-181">Записывает двоичные данные на <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0398-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="d0398-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="d0398-183">Записывает указанную текстовую строку на <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="d0398-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="d0398-184">Новая и расширенная документация</span><span class="sxs-lookup"><span data-stu-id="d0398-184">New and enhanced documentation</span></span>

- <span data-ttu-id="d0398-185">**[Темы примера кода](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="d0398-186">Примеры были расширены, чтобы содержать примеры кода, написанные в Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="d0398-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="d0398-187">Эти примеры кода можно скопировать и вклеить в редактор.</span><span class="sxs-lookup"><span data-stu-id="d0398-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="d0398-188">**[Темы поставщика](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="d0398-189">Включена новая тема, которая объясняет, как использовать ADO с [поставщиком OLE DB для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="d0398-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="d0398-190">**[Программирование с помощью ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="d0398-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="d0398-191">В этом новом разделе содержатся советы и рекомендации по использованию ADO с различными языками программирования.</span><span class="sxs-lookup"><span data-stu-id="d0398-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="d0398-192">Он содержит существующие индексы синтаксиса для расширений Visual C++ для ADO и ADO/WFC, а также новые сведения, специфические для разработчиков, использующих Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ или Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="d0398-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>


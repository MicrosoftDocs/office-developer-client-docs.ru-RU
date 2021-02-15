---
title: Записи и поля от поставщика
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ebbfeb303bb575928f09858db5d3a34cf2171ce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300758"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="63782-102">Записи и поля от поставщика</span><span class="sxs-lookup"><span data-stu-id="63782-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="63782-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63782-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63782-104">При открытом [объекте Record](record-object-ado.md) его источником может быть текущая строка открытого объекта [Recordset,](recordset-object-ado.md)абсолютный URL-адрес или относительный URL-адрес в сочетании с открытым объектом [Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="63782-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="63782-105">Если [](fields-collection-ado.md) запись **открывается** из объекта **Recordset,** коллекция **Полей** объекта Record будет содержать все поля из объекта **Recordset,** а также все поля, добавленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="63782-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="63782-106">Поставщик может вставлять дополнительные поля, которые служат дополнительными характеристиками **записи.**</span><span class="sxs-lookup"><span data-stu-id="63782-106">The provider may insert additional fields that serve as supplementary characteristics of the **Record**.</span></span> <span data-ttu-id="63782-107">В результате запись **может** иметь уникальные  поля, не в  наборе записей в целом, или запись, производная от другой строки **recordset.**</span><span class="sxs-lookup"><span data-stu-id="63782-107">As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="63782-108">Например, все строки объекта **Recordset,** производные от источника данных электронной почты, могут иметь такие столбцы, как From, To и Subject.</span><span class="sxs-lookup"><span data-stu-id="63782-108">For example, all rows of a **Recordset** derived from an email data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="63782-109">Запись, производная от **этого recordset,** будет иметь те же поля. </span><span class="sxs-lookup"><span data-stu-id="63782-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="63782-110">Однако запись **также может** иметь другие поля, уникальные для конкретного сообщения, представленного этой записью, например "Вложение" и "Копия" (копия). </span><span class="sxs-lookup"><span data-stu-id="63782-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="63782-111">Хотя объект **Record** и текущая строка **объекта Recordset** имеют одинаковые поля, они отличаются, так как объекты **Record** и **Recordset** имеют разные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="63782-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="63782-112">Поле, общее для объекта **Record** и **Recordset,** можно изменить в любом объекте.</span><span class="sxs-lookup"><span data-stu-id="63782-112">A field held in common by the **Record** and **Recordset** can be modified on either object.</span></span> <span data-ttu-id="63782-113">Однако поле не может быть удалено в объекте **Record,** хотя поставщик может поддерживать установку для поля null.</span><span class="sxs-lookup"><span data-stu-id="63782-113">However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="63782-114">После открытия **записи** можно добавить поля программным путем.</span><span class="sxs-lookup"><span data-stu-id="63782-114">After the **Record** is opened, you can programmatically add fields.</span></span> <span data-ttu-id="63782-115">Вы также можете удалить добавленные поля, но нельзя удалить поля из исходного **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="63782-115">You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="63782-116">Вы также можете открыть объект **Record** непосредственно из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="63782-116">You may also open the **Record** object directly from a URL.</span></span> <span data-ttu-id="63782-117">В этом случае поля, добавленные в **запись,** зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="63782-117">In this case, the fields added to the **Record** depend on the underlying provider.</span></span> <span data-ttu-id="63782-118">В настоящее время большинство поставщиков добавляют набор полей, которые описывают сущность, представленную **записью.**</span><span class="sxs-lookup"><span data-stu-id="63782-118">Currently, most providers add a set of fields that describe the entity represented by the **Record**.</span></span> <span data-ttu-id="63782-119">Если сущность состоит из потока ветвей, например простого файла, объект [Stream](stream-object-ado.md) обычно можно открыть из **записи.**</span><span class="sxs-lookup"><span data-stu-id="63782-119">If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="63782-120">Специальные поля для поставщиков источников документов</span><span class="sxs-lookup"><span data-stu-id="63782-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="63782-121">Особый класс поставщиков, называемый *поставщиками* источников документов, управляет папками и документами.</span><span class="sxs-lookup"><span data-stu-id="63782-121">A special class of providers, called *document source providers*, manages folders and documents.</span></span> <span data-ttu-id="63782-122">Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источника документов заполняет эти объекты уникальным набором полей, описывая характеристики документа, а не сам документ.</span><span class="sxs-lookup"><span data-stu-id="63782-122">When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</span></span> <span data-ttu-id="63782-123">Как правило, одно поле содержит ссылку на **поток,** который представляет документ.</span><span class="sxs-lookup"><span data-stu-id="63782-123">Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="63782-124">Эти поля составляют **запись** ресурса или набор **записей** и перечислены для определенных поставщиков, которые их поддерживают, в приложении [А. Поставщики.](appendix-a-providers.md)</span><span class="sxs-lookup"><span data-stu-id="63782-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="63782-125">Две константы индексировали коллекцию **Fields** записи ресурса или **recordset,** чтобы получить пару часто используемых полей. </span><span class="sxs-lookup"><span data-stu-id="63782-125">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields.</span></span> <span data-ttu-id="63782-126">Свойство **Field** object [Value](value-property-ado.md) возвращает нужное содержимое.</span><span class="sxs-lookup"><span data-stu-id="63782-126">The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="63782-127">Поле, к которое можно получить доступ с помощью **константы adDefaultStream,** содержит поток по умолчанию, связанный с объектом **Record** или **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="63782-127">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object.</span></span> <span data-ttu-id="63782-128">Поставщик назначает объекту поток по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63782-128">The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="63782-129">Поле, к которое можно получить доступ с помощью **константы adRecordURL,** содержит абсолютный URL-адрес, идентифицируя документ.</span><span class="sxs-lookup"><span data-stu-id="63782-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="63782-130">Поставщик источника документов не поддерживает коллекцию [свойств](properties-collection-ado.md) объектов **Record** и **Field.**</span><span class="sxs-lookup"><span data-stu-id="63782-130">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects.</span></span> <span data-ttu-id="63782-131">Для таких объектов содержимое коллекции **Properties** имеет null.</span><span class="sxs-lookup"><span data-stu-id="63782-131">The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="63782-132">Поставщик источника документов может добавить свойство для конкретного поставщика, например **Datasource Type,** чтобы определить, является ли он поставщиком источника документов.</span><span class="sxs-lookup"><span data-stu-id="63782-132">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider.</span></span> <span data-ttu-id="63782-133">Дополнительные сведения о том, как определить тип поставщика, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="63782-133">For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="63782-134">Столбцы наборов записей ресурсов</span><span class="sxs-lookup"><span data-stu-id="63782-134">Resource Recordset Columns</span></span>

<span data-ttu-id="63782-135">Набор *записей ресурсов* состоит из следующих столбцов.</span><span class="sxs-lookup"><span data-stu-id="63782-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63782-136">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="63782-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="63782-137">Тип</span><span class="sxs-lookup"><span data-stu-id="63782-137">Type</span></span></p></th>
<th><p><span data-ttu-id="63782-138">Описание</span><span class="sxs-lookup"><span data-stu-id="63782-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63782-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="63782-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="63782-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-141">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-141">Read-only.</span></span> <span data-ttu-id="63782-142">Указывает URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-142">Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="63782-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="63782-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-145">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-145">Read-only.</span></span> <span data-ttu-id="63782-146">Указывает абсолютный URL-адрес родительской записи.</span><span class="sxs-lookup"><span data-stu-id="63782-146">Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="63782-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="63782-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-149">Read-only.</span></span> <span data-ttu-id="63782-150">Указывает абсолютный URL-адрес ресурса, который является совмещением PARENTNAME и PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="63782-150">Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="63782-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="63782-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="63782-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="63782-153">Имеет true, если ресурс скрыт.</span><span class="sxs-lookup"><span data-stu-id="63782-153">True if the resource is hidden.</span></span> <span data-ttu-id="63782-154">Никакие строки не возвращаются, если команда, создав набор строк, явным образом не выберет строки, RESOURCE_ISHIDDEN имеет RESOURCE_ISHIDDEN true.</span><span class="sxs-lookup"><span data-stu-id="63782-154">No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="63782-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="63782-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="63782-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="63782-157">Имеет true, если ресурс находится только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-157">True if the resource is read-only.</span></span> <span data-ttu-id="63782-158">Пытается открыть этот ресурс с помощью DBBINDFLAG_WRITE и не удастся с DB_E_READONLY.</span><span class="sxs-lookup"><span data-stu-id="63782-158">Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</span></span> <span data-ttu-id="63782-159">Это свойство может быть изменено, даже если ресурс открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-159">This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="63782-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="63782-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-162">Указывает вероятное использование документа, например краткое извект юриста.</span><span class="sxs-lookup"><span data-stu-id="63782-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="63782-163">Это может соответствовать шаблону Office, используемму для создания документа.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="63782-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="63782-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="63782-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-166">Указывает тип MIME документа, указывающий формат, например &quot; текст или &quot; html.'</span><span class="sxs-lookup"><span data-stu-id="63782-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="63782-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="63782-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-169">Указывает язык, на котором хранится содержимое.</span><span class="sxs-lookup"><span data-stu-id="63782-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="63782-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="63782-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="63782-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="63782-172">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-172">Read-only.</span></span> <span data-ttu-id="63782-173">Указывает структуру FILETIME, содержащую время создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-173">Indicates a FILETIME structure containing the time the resource was created.</span></span> <span data-ttu-id="63782-174">Время сообщается в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="63782-174">The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="63782-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="63782-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="63782-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="63782-177">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-177">Read-only.</span></span> <span data-ttu-id="63782-178">Указывает структуру FILETIME, содержащую время последнего доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="63782-178">Indicates a FILETIME structure containing the time that the resource was last accessed.</span></span> <span data-ttu-id="63782-179">Время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="63782-179">The time is in UTC format.</span></span> <span data-ttu-id="63782-180">Если поставщик не поддерживает этот член времени, то члены FILETIME имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="63782-180">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="63782-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="63782-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="63782-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="63782-183">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-183">Read-only.</span></span> <span data-ttu-id="63782-184">Указывает структуру FILETIME, содержащую время последней работы ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-184">Indicates a FILETIME structure containing the time that the resource was last written.</span></span> <span data-ttu-id="63782-185">Время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="63782-185">The time is in UTC format.</span></span> <span data-ttu-id="63782-186">Если поставщик не поддерживает этот член времени, то члены FILETIME имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="63782-186">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="63782-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="63782-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="63782-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="63782-189">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-189">Read-only.</span></span> <span data-ttu-id="63782-190">Указывает размер потока ресурса по умолчанию в ветвях.</span><span class="sxs-lookup"><span data-stu-id="63782-190">Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="63782-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="63782-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="63782-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="63782-193">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-193">Read-only.</span></span> <span data-ttu-id="63782-194">Имеет true, если ресурс является коллекцией, например каталогом.</span><span class="sxs-lookup"><span data-stu-id="63782-194">True if the resource is a collection, such as a directory.</span></span> <span data-ttu-id="63782-195">False, если ресурс является простым файлом.</span><span class="sxs-lookup"><span data-stu-id="63782-195">False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="63782-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="63782-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="63782-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="63782-198">Имеет true, если ресурс является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="63782-198">True if the resource is a structured document.</span></span> <span data-ttu-id="63782-199">False, если ресурс не является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="63782-199">False if the resource is not a structured document.</span></span> <span data-ttu-id="63782-200">Это может быть коллекция или простой файл.</span><span class="sxs-lookup"><span data-stu-id="63782-200">It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="63782-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="63782-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-203">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-203">Read-only.</span></span> <span data-ttu-id="63782-204">Указывает, что этот ресурс содержит URL-адрес простого документа папки или структурированного документа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63782-204">Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</span></span> <span data-ttu-id="63782-205">Используется, когда поток по умолчанию запрашивается у ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-205">Used when the default stream is requested from a resource.</span></span> <span data-ttu-id="63782-206">Это свойство не является пустым для простого файла.</span><span class="sxs-lookup"><span data-stu-id="63782-206">This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="63782-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="63782-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="63782-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="63782-209">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-209">Read-only.</span></span> <span data-ttu-id="63782-210">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="63782-210">Optional.</span></span> <span data-ttu-id="63782-211">Указывает главу строки, содержащей детей ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-211">Indicates the chapter of the rowset containing the children of the resource.</span></span> <span data-ttu-id="63782-212">(Поставщик <em>OLE DB для публикации</em> в Интернете не использует этот столбец.)</span><span class="sxs-lookup"><span data-stu-id="63782-212">(The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63782-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="63782-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="63782-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="63782-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="63782-215">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-215">Read-only.</span></span> <span data-ttu-id="63782-216">Указывает отображаемую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="63782-216">Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63782-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="63782-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="63782-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="63782-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="63782-219">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63782-219">Read-only.</span></span> <span data-ttu-id="63782-220">Имеет true, если ресурс является корнем коллекции или структурированного документа.</span><span class="sxs-lookup"><span data-stu-id="63782-220">True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>


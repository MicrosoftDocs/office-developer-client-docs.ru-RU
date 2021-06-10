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
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="b8760-102">Записи и поля от поставщика</span><span class="sxs-lookup"><span data-stu-id="b8760-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="b8760-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8760-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8760-104">Когда объект [Record](record-object-ado.md) открыт, его источником может быть текущая строка открытого наборов записей, [](recordset-object-ado.md)абсолютный URL-адрес или относительный URL-адрес в сочетании с объектом open [Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b8760-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="b8760-105">Если **запись** открыта из **recordset,**  коллекция [](fields-collection-ado.md) Полей объектов Record будет содержать все поля из **Recordset,** а также все поля, добавленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="b8760-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="b8760-106">Поставщик может вставить дополнительные поля, которые служат дополнительными характеристиками **записи.**</span><span class="sxs-lookup"><span data-stu-id="b8760-106">The provider may insert additional fields that serve as supplementary characteristics of the **Record**.</span></span> <span data-ttu-id="b8760-107">В результате запись **может** иметь уникальные поля не в **наборе Recordset** в целом или записи, полученные из другой строки **Recordset.** </span><span class="sxs-lookup"><span data-stu-id="b8760-107">As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="b8760-108">Например, все строки **наборов записей,** полученные из источника данных электронной почты, могут иметь столбцы, такие как From, To и Subject.</span><span class="sxs-lookup"><span data-stu-id="b8760-108">For example, all rows of a **Recordset** derived from an email data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="b8760-109">Запись, полученная из **этого Набор записей,** будет иметь те же поля. </span><span class="sxs-lookup"><span data-stu-id="b8760-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="b8760-110">Тем не менее, **запись** также может иметь другие поля, уникальные для конкретного сообщения, представленного этой записью, например вложения и Cc (копия углерода).</span><span class="sxs-lookup"><span data-stu-id="b8760-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="b8760-111">Несмотря на **то,** что объект Record и текущая строка **наборов Записей** имеют те же поля, они отличаются, так как объекты **Record** и **Recordset** имеют различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="b8760-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="b8760-112">Поле, общее для **записи** и **наборов записей,** может быть изменено на любом объекте.</span><span class="sxs-lookup"><span data-stu-id="b8760-112">A field held in common by the **Record** and **Recordset** can be modified on either object.</span></span> <span data-ttu-id="b8760-113">Однако поле не может быть удалено на **объекте Запись,** хотя поставщик может поддерживать установку поля на null.</span><span class="sxs-lookup"><span data-stu-id="b8760-113">However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="b8760-114">После открытия **записи** можно программным образом добавлять поля.</span><span class="sxs-lookup"><span data-stu-id="b8760-114">After the **Record** is opened, you can programmatically add fields.</span></span> <span data-ttu-id="b8760-115">Кроме того, можно удалить добавленные поля, но нельзя удалить поля из исходного **набора Записей.**</span><span class="sxs-lookup"><span data-stu-id="b8760-115">You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="b8760-116">Вы также можете открыть **объект Запись** непосредственно из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b8760-116">You may also open the **Record** object directly from a URL.</span></span> <span data-ttu-id="b8760-117">В этом случае поля, добавленные в **Запись,** зависят от поставщика.</span><span class="sxs-lookup"><span data-stu-id="b8760-117">In this case, the fields added to the **Record** depend on the underlying provider.</span></span> <span data-ttu-id="b8760-118">В настоящее время большинство поставщиков добавляют набор полей, описывая сущность, представленную **записью.**</span><span class="sxs-lookup"><span data-stu-id="b8760-118">Currently, most providers add a set of fields that describe the entity represented by the **Record**.</span></span> <span data-ttu-id="b8760-119">Если объект состоит из потока bytes, например простого файла, объект [Stream](stream-object-ado.md) обычно можно открыть из **записи.**</span><span class="sxs-lookup"><span data-stu-id="b8760-119">If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="b8760-120">Специальные поля для поставщиков источников документов</span><span class="sxs-lookup"><span data-stu-id="b8760-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="b8760-121">Специальный класс поставщиков, называемых поставщиками источников *документов,* управляет папками и документами.</span><span class="sxs-lookup"><span data-stu-id="b8760-121">A special class of providers, called *document source providers*, manages folders and documents.</span></span> <span data-ttu-id="b8760-122">Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источников документов заполняет эти объекты уникальным набором полей, описывая характеристики документа, а не сам документ.</span><span class="sxs-lookup"><span data-stu-id="b8760-122">When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</span></span> <span data-ttu-id="b8760-123">Как правило, одно поле содержит ссылку на **поток,** который представляет документ.</span><span class="sxs-lookup"><span data-stu-id="b8760-123">Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="b8760-124">Эти поля представляют собой запись **ресурсов** или **набор записей** и перечислены для определенных поставщиков, которые поддерживают их в [приложении A: Providers.](appendix-a-providers.md)</span><span class="sxs-lookup"><span data-stu-id="b8760-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="b8760-125">Две константы индексировали коллекцию **Полей** записи **ресурсов** или **Набор** записей, чтобы получить пару часто используемых полей.</span><span class="sxs-lookup"><span data-stu-id="b8760-125">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields.</span></span> <span data-ttu-id="b8760-126">Свойство **Значение** объекта [Field](value-property-ado.md) возвращает нужное содержимое.</span><span class="sxs-lookup"><span data-stu-id="b8760-126">The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="b8760-127">Поле с константой **adDefaultStream** содержит поток по умолчанию, связанный с объектом **Record** или **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b8760-127">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object.</span></span> <span data-ttu-id="b8760-128">Поставщик назначает объекту поток по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8760-128">The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="b8760-129">Поле с константой **adRecordURL** содержит абсолютный URL-адрес, идентифицирует документ.</span><span class="sxs-lookup"><span data-stu-id="b8760-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="b8760-130">Поставщик источников документов не поддерживает коллекцию [свойств](properties-collection-ado.md) объектов **Записи** и **Поля.**</span><span class="sxs-lookup"><span data-stu-id="b8760-130">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects.</span></span> <span data-ttu-id="b8760-131">Содержимое коллекции **Свойств** является null для таких объектов.</span><span class="sxs-lookup"><span data-stu-id="b8760-131">The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="b8760-132">Поставщик источника документов может добавить свойство, определенное для поставщика, например **Тип Datasource,** чтобы определить, является ли он поставщиком исходных документов.</span><span class="sxs-lookup"><span data-stu-id="b8760-132">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider.</span></span> <span data-ttu-id="b8760-133">Дополнительные сведения о том, как определить тип поставщика, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="b8760-133">For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="b8760-134">Столбцы записи ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8760-134">Resource Recordset Columns</span></span>

<span data-ttu-id="b8760-135">Набор *записей ресурсов* состоит из следующих столбцов.</span><span class="sxs-lookup"><span data-stu-id="b8760-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8760-136">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="b8760-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="b8760-137">Тип</span><span class="sxs-lookup"><span data-stu-id="b8760-137">Type</span></span></p></th>
<th><p><span data-ttu-id="b8760-138">Описание</span><span class="sxs-lookup"><span data-stu-id="b8760-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8760-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="b8760-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="b8760-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-141">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-141">Read-only.</span></span> <span data-ttu-id="b8760-142">Указывает URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-142">Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="b8760-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="b8760-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-145">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-145">Read-only.</span></span> <span data-ttu-id="b8760-146">Указывает абсолютный URL-адрес родительской записи.</span><span class="sxs-lookup"><span data-stu-id="b8760-146">Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="b8760-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="b8760-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-149">Read-only.</span></span> <span data-ttu-id="b8760-150">Указывает абсолютный URL-адрес ресурса, который является concatenation PARENTNAME и PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="b8760-150">Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="b8760-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="b8760-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="b8760-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="b8760-153">True, если ресурс скрыт.</span><span class="sxs-lookup"><span data-stu-id="b8760-153">True if the resource is hidden.</span></span> <span data-ttu-id="b8760-154">Никакие строки не возвращаются, если команда, создав набор строк, явно не выбирает строки, RESOURCE_ISHIDDEN является True.</span><span class="sxs-lookup"><span data-stu-id="b8760-154">No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="b8760-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="b8760-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="b8760-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="b8760-157">True, если ресурс только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-157">True if the resource is read-only.</span></span> <span data-ttu-id="b8760-158">Попытки открыть этот ресурс с помощью DBBINDFLAG_WRITE и сбой с DB_E_READONLY.</span><span class="sxs-lookup"><span data-stu-id="b8760-158">Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</span></span> <span data-ttu-id="b8760-159">Это свойство может быть изменено даже в том случае, если ресурс открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-159">This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="b8760-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="b8760-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-162">Указывает вероятное использование документа , например, краткий обзор юриста.</span><span class="sxs-lookup"><span data-stu-id="b8760-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="b8760-163">Это может соответствовать шаблону Office, используемой для создания документа.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="b8760-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="b8760-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="b8760-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-166">Указывает тип документа MIME, указывающее такой формат, как &quot; text/html &quot; .'</span><span class="sxs-lookup"><span data-stu-id="b8760-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="b8760-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="b8760-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-169">Указывает язык, на котором хранится содержимое.</span><span class="sxs-lookup"><span data-stu-id="b8760-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="b8760-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="b8760-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="b8760-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="b8760-172">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-172">Read-only.</span></span> <span data-ttu-id="b8760-173">Указывает структуру FILETIME, содержащую время создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-173">Indicates a FILETIME structure containing the time the resource was created.</span></span> <span data-ttu-id="b8760-174">Время сообщается в формате Скоординированное универсальное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="b8760-174">The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="b8760-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="b8760-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="b8760-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="b8760-177">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-177">Read-only.</span></span> <span data-ttu-id="b8760-178">Указывает структуру FILETIME, содержащую время последнего доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="b8760-178">Indicates a FILETIME structure containing the time that the resource was last accessed.</span></span> <span data-ttu-id="b8760-179">Время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="b8760-179">The time is in UTC format.</span></span> <span data-ttu-id="b8760-180">Если поставщик не поддерживает этого участника, участники FILETIME ноль.</span><span class="sxs-lookup"><span data-stu-id="b8760-180">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="b8760-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="b8760-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="b8760-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="b8760-183">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-183">Read-only.</span></span> <span data-ttu-id="b8760-184">Указывает структуру FILETIME, содержащую время последней работы ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-184">Indicates a FILETIME structure containing the time that the resource was last written.</span></span> <span data-ttu-id="b8760-185">Время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="b8760-185">The time is in UTC format.</span></span> <span data-ttu-id="b8760-186">Если поставщик не поддерживает этого участника, участники FILETIME ноль.</span><span class="sxs-lookup"><span data-stu-id="b8760-186">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="b8760-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="b8760-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="b8760-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="b8760-189">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-189">Read-only.</span></span> <span data-ttu-id="b8760-190">Указывает размер потока по умолчанию ресурса в bytes.</span><span class="sxs-lookup"><span data-stu-id="b8760-190">Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="b8760-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="b8760-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="b8760-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="b8760-193">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-193">Read-only.</span></span> <span data-ttu-id="b8760-194">True, если ресурс — это коллекция, например каталог.</span><span class="sxs-lookup"><span data-stu-id="b8760-194">True if the resource is a collection, such as a directory.</span></span> <span data-ttu-id="b8760-195">False, если ресурс является простым файлом.</span><span class="sxs-lookup"><span data-stu-id="b8760-195">False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="b8760-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="b8760-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="b8760-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="b8760-198">True, если ресурс является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="b8760-198">True if the resource is a structured document.</span></span> <span data-ttu-id="b8760-199">False, если ресурс не является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="b8760-199">False if the resource is not a structured document.</span></span> <span data-ttu-id="b8760-200">Это может быть коллекция или простой файл.</span><span class="sxs-lookup"><span data-stu-id="b8760-200">It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="b8760-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="b8760-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-203">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-203">Read-only.</span></span> <span data-ttu-id="b8760-204">Указывает, что этот ресурс содержит URL-адрес простого документа папки или структурированного документа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8760-204">Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</span></span> <span data-ttu-id="b8760-205">Используется при запросе потока по умолчанию из ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-205">Used when the default stream is requested from a resource.</span></span> <span data-ttu-id="b8760-206">Это свойство пусто для простого файла.</span><span class="sxs-lookup"><span data-stu-id="b8760-206">This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="b8760-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="b8760-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="b8760-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="b8760-209">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-209">Read-only.</span></span> <span data-ttu-id="b8760-210">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b8760-210">Optional.</span></span> <span data-ttu-id="b8760-211">Указывает главу строки, содержащую дети ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-211">Indicates the chapter of the rowset containing the children of the resource.</span></span> <span data-ttu-id="b8760-212">(Поставщик <em>OLE DB для публикации в Интернете</em> не использует этот столбец.)</span><span class="sxs-lookup"><span data-stu-id="b8760-212">(The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8760-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="b8760-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="b8760-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="b8760-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="b8760-215">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-215">Read-only.</span></span> <span data-ttu-id="b8760-216">Указывает имя отображения ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8760-216">Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8760-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="b8760-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="b8760-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="b8760-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="b8760-219">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8760-219">Read-only.</span></span> <span data-ttu-id="b8760-220">True, если ресурс является корнем коллекции или структурированного документа.</span><span class="sxs-lookup"><span data-stu-id="b8760-220">True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>


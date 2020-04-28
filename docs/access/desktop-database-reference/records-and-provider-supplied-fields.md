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
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="06800-102">Записи и поля от поставщика</span><span class="sxs-lookup"><span data-stu-id="06800-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="06800-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06800-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06800-104">Когда открыт объект [Record](record-object-ado.md) , его источник может быть текущей строкой открытого [набора записей](recordset-object-ado.md), абсолютным URL-адресом или относительным URL-адресом в сочетании с открытым объектом [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="06800-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="06800-105">Если **запись** открыта из объекта **Recordset**, коллекция [Fields](fields-collection-ado.md) объекта **Record** будет содержать все поля из **набора записей**, а также все поля, добавленные базовым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="06800-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="06800-106">Поставщик может вставлять дополнительные поля, которые используются в качестве дополнительных характеристик **записи**.</span><span class="sxs-lookup"><span data-stu-id="06800-106">The provider may insert additional fields that serve as supplementary characteristics of the **Record**.</span></span> <span data-ttu-id="06800-107">В результате у **записи** могут быть уникальные поля, не содержащиеся в **наборе записей** в целом, или любая **запись** , полученная из другой строки **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="06800-107">As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="06800-108">Например, все строки объекта **Recordset** , полученные из источника данных электронной почты, могут иметь такие столбцы, как from, to и subject.</span><span class="sxs-lookup"><span data-stu-id="06800-108">For example, all rows of a **Recordset** derived from an email data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="06800-109">У **записи** , полученной из этого **набора записей** , будут одинаковые поля.</span><span class="sxs-lookup"><span data-stu-id="06800-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="06800-110">Однако **запись** также может иметь другие поля, уникальные для конкретного сообщения, представленного этой **записью**, например "вложение" и "копия" (копия).</span><span class="sxs-lookup"><span data-stu-id="06800-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="06800-111">Несмотря на то, что объект **Record** и текущая строка **набора записей** имеют одинаковые поля, они отличаются, так как **записи** и объекты **Recordset** имеют различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="06800-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="06800-112">Поле, содержащееся в общей **записи** и **наборе записей** , можно изменить для любого объекта.</span><span class="sxs-lookup"><span data-stu-id="06800-112">A field held in common by the **Record** and **Recordset** can be modified on either object.</span></span> <span data-ttu-id="06800-113">Однако поле не может быть удалено из объекта **Record** , хотя базовый поставщик может поддерживать установку для поля значения NULL.</span><span class="sxs-lookup"><span data-stu-id="06800-113">However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="06800-114">После открытия **записи** можно программным способом добавлять поля.</span><span class="sxs-lookup"><span data-stu-id="06800-114">After the **Record** is opened, you can programmatically add fields.</span></span> <span data-ttu-id="06800-115">Вы также можете удалять поля, которые вы добавили, но не можете удалять поля из исходного объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="06800-115">You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="06800-116">Кроме того, вы можете открыть объект **Record** непосредственно из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="06800-116">You may also open the **Record** object directly from a URL.</span></span> <span data-ttu-id="06800-117">В этом случае поля, добавленные к **записи** , зависят от базового поставщика.</span><span class="sxs-lookup"><span data-stu-id="06800-117">In this case, the fields added to the **Record** depend on the underlying provider.</span></span> <span data-ttu-id="06800-118">В настоящее время большинство поставщиков добавляют набор полей, описывающих объект, представленный **записью**.</span><span class="sxs-lookup"><span data-stu-id="06800-118">Currently, most providers add a set of fields that describe the entity represented by the **Record**.</span></span> <span data-ttu-id="06800-119">Если сущность состоит из потока байтов, например простого файла, то объект [Stream](stream-object-ado.md) обычно можно открыть из **записи**.</span><span class="sxs-lookup"><span data-stu-id="06800-119">If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="06800-120">Специальные поля для поставщиков источника документов</span><span class="sxs-lookup"><span data-stu-id="06800-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="06800-121">Особый класс поставщиков, называемый *поставщиками источника документов*, управляет папками и документами.</span><span class="sxs-lookup"><span data-stu-id="06800-121">A special class of providers, called *document source providers*, manages folders and documents.</span></span> <span data-ttu-id="06800-122">Когда объект **Record** представляет документ или объект **Recordset** представляет папку документов, поставщик источника документа заполняет эти объекты уникальным набором полей, описывающих характеристики документа, а не собственно сам документ.</span><span class="sxs-lookup"><span data-stu-id="06800-122">When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</span></span> <span data-ttu-id="06800-123">Как правило, одно поле содержит ссылку на **поток** , представляющий документ.</span><span class="sxs-lookup"><span data-stu-id="06800-123">Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="06800-124">Эти поля составляют **запись** ресурса или **набор записей** и отображаются для определенных поставщиков, которые их поддерживают в [приложении a: providers](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="06800-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="06800-125">Два константа — индексирует коллекцию **Fields** **записи** ресурса или **набора записей** , чтобы получить сочетание часто используемых полей.</span><span class="sxs-lookup"><span data-stu-id="06800-125">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields.</span></span> <span data-ttu-id="06800-126">Свойство [value](value-property-ado.md) объекта **field** возвращает нужное содержимое.</span><span class="sxs-lookup"><span data-stu-id="06800-126">The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="06800-127">Поле, доступное с константой **аддефаултстреам** , содержит поток по умолчанию, связанный с **записью** или объектом **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="06800-127">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object.</span></span> <span data-ttu-id="06800-128">Поставщик назначает поток по умолчанию объекту.</span><span class="sxs-lookup"><span data-stu-id="06800-128">The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="06800-129">Поле, доступное с константой **адрекордурл** , содержит абсолютный URL-адрес, идентифицирующий документ.</span><span class="sxs-lookup"><span data-stu-id="06800-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="06800-130">Поставщик источника документов не поддерживает коллекцию [свойств](properties-collection-ado.md) объектов **Record** и **field** .</span><span class="sxs-lookup"><span data-stu-id="06800-130">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects.</span></span> <span data-ttu-id="06800-131">Для таких объектов содержимое коллекции **Properties** равно null.</span><span class="sxs-lookup"><span data-stu-id="06800-131">The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="06800-132">Поставщик источника документов может добавить зависящее от поставщика свойство, например **Тип DataSource** , чтобы определить, является ли он поставщиком источника документа.</span><span class="sxs-lookup"><span data-stu-id="06800-132">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider.</span></span> <span data-ttu-id="06800-133">Дополнительные сведения о том, как определить тип поставщика, можно найти в документации по поставщику.</span><span class="sxs-lookup"><span data-stu-id="06800-133">For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="06800-134">Столбцы "набор записей ресурса"</span><span class="sxs-lookup"><span data-stu-id="06800-134">Resource Recordset Columns</span></span>

<span data-ttu-id="06800-135">*Набор записей ресурсов* состоит из следующих столбцов.</span><span class="sxs-lookup"><span data-stu-id="06800-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06800-136">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="06800-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="06800-137">Тип</span><span class="sxs-lookup"><span data-stu-id="06800-137">Type</span></span></p></th>
<th><p><span data-ttu-id="06800-138">Описание</span><span class="sxs-lookup"><span data-stu-id="06800-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06800-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="06800-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="06800-140">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-141">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-141">Read-only.</span></span> <span data-ttu-id="06800-142">Указывает URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="06800-142">Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="06800-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="06800-144">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-145">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-145">Read-only.</span></span> <span data-ttu-id="06800-146">Указывает абсолютный URL-адрес родительской записи.</span><span class="sxs-lookup"><span data-stu-id="06800-146">Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="06800-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="06800-148">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-149">Read-only.</span></span> <span data-ttu-id="06800-150">Указывает абсолютный URL-адрес ресурса, который является объединением ПАРЕНТНАМЕ и ПАРСЕНАМЕ.</span><span class="sxs-lookup"><span data-stu-id="06800-150">Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="06800-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="06800-152">адбулеан</span><span class="sxs-lookup"><span data-stu-id="06800-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="06800-153">Значение true, если ресурс скрыт.</span><span class="sxs-lookup"><span data-stu-id="06800-153">True if the resource is hidden.</span></span> <span data-ttu-id="06800-154">Никакие строки не возвращаются, если команда, создающая набор строк, явно не выбирает строки, где RESOURCE_ISHIDDEN имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="06800-154">No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="06800-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="06800-156">адбулеан</span><span class="sxs-lookup"><span data-stu-id="06800-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="06800-157">Значение true, если ресурс доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-157">True if the resource is read-only.</span></span> <span data-ttu-id="06800-158">Попытки открыть этот ресурс с помощью DBBINDFLAG_WRITE и DB_E_READONLY будут неудачными.</span><span class="sxs-lookup"><span data-stu-id="06800-158">Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</span></span> <span data-ttu-id="06800-159">Это свойство можно редактировать, даже если ресурс открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-159">This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="06800-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="06800-161">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-162">Указывает на вероятность использования документа, например, юрист.</span><span class="sxs-lookup"><span data-stu-id="06800-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="06800-163">Это может соответствовать шаблону Office, используемому для создания документа.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="06800-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="06800-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="06800-165">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-166">Указывает тип MIME документа, указывающий формат, например &quot;Text/HTML&quot;. '</span><span class="sxs-lookup"><span data-stu-id="06800-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="06800-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="06800-168">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-169">Указывает язык, на котором хранится контент.</span><span class="sxs-lookup"><span data-stu-id="06800-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="06800-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="06800-171">адфилетиме</span><span class="sxs-lookup"><span data-stu-id="06800-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="06800-172">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-172">Read-only.</span></span> <span data-ttu-id="06800-173">Указывает структуру FILETIME, содержащую время создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="06800-173">Indicates a FILETIME structure containing the time the resource was created.</span></span> <span data-ttu-id="06800-174">Время отображается в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="06800-174">The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="06800-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="06800-176">адфилетиме</span><span class="sxs-lookup"><span data-stu-id="06800-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="06800-177">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-177">Read-only.</span></span> <span data-ttu-id="06800-178">Указывает структуру FILETIME, содержащую время последнего доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="06800-178">Indicates a FILETIME structure containing the time that the resource was last accessed.</span></span> <span data-ttu-id="06800-179">Время задается в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="06800-179">The time is in UTC format.</span></span> <span data-ttu-id="06800-180">Если поставщик не поддерживает этот элемент времени, элементы FILETIME равны нулю.</span><span class="sxs-lookup"><span data-stu-id="06800-180">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="06800-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="06800-182">адфилетиме</span><span class="sxs-lookup"><span data-stu-id="06800-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="06800-183">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-183">Read-only.</span></span> <span data-ttu-id="06800-184">Указывает структуру FILETIME, содержащую время последней записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="06800-184">Indicates a FILETIME structure containing the time that the resource was last written.</span></span> <span data-ttu-id="06800-185">Время задается в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="06800-185">The time is in UTC format.</span></span> <span data-ttu-id="06800-186">Если поставщик не поддерживает этот элемент времени, элементы FILETIME равны нулю.</span><span class="sxs-lookup"><span data-stu-id="06800-186">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="06800-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="06800-188">асунсигнедбигинт</span><span class="sxs-lookup"><span data-stu-id="06800-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="06800-189">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-189">Read-only.</span></span> <span data-ttu-id="06800-190">Указывает размер потока ресурсов по умолчанию (в байтах).</span><span class="sxs-lookup"><span data-stu-id="06800-190">Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="06800-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="06800-192">адбулеан</span><span class="sxs-lookup"><span data-stu-id="06800-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="06800-193">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-193">Read-only.</span></span> <span data-ttu-id="06800-194">Значение true, если ресурс является коллекцией, например каталогом.</span><span class="sxs-lookup"><span data-stu-id="06800-194">True if the resource is a collection, such as a directory.</span></span> <span data-ttu-id="06800-195">False, если ресурс является простым файлом.</span><span class="sxs-lookup"><span data-stu-id="06800-195">False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="06800-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="06800-197">адбулеан</span><span class="sxs-lookup"><span data-stu-id="06800-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="06800-198">Значение true, если ресурс является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="06800-198">True if the resource is a structured document.</span></span> <span data-ttu-id="06800-199">False, если ресурс не является структурированным документом.</span><span class="sxs-lookup"><span data-stu-id="06800-199">False if the resource is not a structured document.</span></span> <span data-ttu-id="06800-200">Это может быть коллекция или простой файл.</span><span class="sxs-lookup"><span data-stu-id="06800-200">It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="06800-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="06800-202">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-203">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-203">Read-only.</span></span> <span data-ttu-id="06800-204">Указывает, что этот ресурс содержит URL-адрес простого документа по умолчанию папки или структурированного документа.</span><span class="sxs-lookup"><span data-stu-id="06800-204">Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</span></span> <span data-ttu-id="06800-205">Используется, когда для ресурса запрашивается поток по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="06800-205">Used when the default stream is requested from a resource.</span></span> <span data-ttu-id="06800-206">Это свойство не заполнено для простого файла.</span><span class="sxs-lookup"><span data-stu-id="06800-206">This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="06800-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="06800-208">адчаптер</span><span class="sxs-lookup"><span data-stu-id="06800-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="06800-209">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-209">Read-only.</span></span> <span data-ttu-id="06800-210">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="06800-210">Optional.</span></span> <span data-ttu-id="06800-211">Указывает раздел набора строк, содержащий дочерние элементы ресурса.</span><span class="sxs-lookup"><span data-stu-id="06800-211">Indicates the chapter of the rowset containing the children of the resource.</span></span> <span data-ttu-id="06800-212">( <em>Поставщик OLE DB для публикации в Интернете</em> не использует этот столбец.)</span><span class="sxs-lookup"><span data-stu-id="06800-212">(The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06800-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="06800-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="06800-214">адварвчар</span><span class="sxs-lookup"><span data-stu-id="06800-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="06800-215">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-215">Read-only.</span></span> <span data-ttu-id="06800-216">Указывает отображаемое имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="06800-216">Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06800-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="06800-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="06800-218">адбулеан</span><span class="sxs-lookup"><span data-stu-id="06800-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="06800-219">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06800-219">Read-only.</span></span> <span data-ttu-id="06800-220">Значение true, если ресурс является корнем коллекции или структурированного документа.</span><span class="sxs-lookup"><span data-stu-id="06800-220">True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>


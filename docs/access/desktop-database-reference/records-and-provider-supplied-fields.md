---
title: Записи и поля указано поставщика
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2de9f48b9f35afb208006118add97c9b29c4885
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944524"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="d2c0b-102">Записи и поля указано поставщика</span><span class="sxs-lookup"><span data-stu-id="d2c0b-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="d2c0b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2c0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2c0b-104">При открытии объект [записи](record-object-ado.md) источника может быть текущей строки open [записей](recordset-object-ado.md), абсолютный URL-адрес или относительный URL-адрес в сочетании с помощью open объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d2c0b-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="d2c0b-105">Если **запись** открывается из **набора записей**, объект **записи** коллекции [полей](fields-collection-ado.md) будет содержать все поля из **набора записей**, а также все поля, добавляемые в основной поставщик.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="d2c0b-106">Поставщик может вставить дополнительные поля, которые используются в качестве дополнительных характеристики **записи**.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-106">The provider may insert additional fields that serve as supplementary characteristics of the **Record**.</span></span> <span data-ttu-id="d2c0b-107">В результате **записи** может иметь уникальные поля не в **записей** в целом или любой **записи** , производного от другого строки набора **записей**.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-107">As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="d2c0b-108">Например все строки из **набора записей** , производного от источника данных электронной почты может, чтобы иметь столбцов, например, в и тема.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-108">For example, all rows of a **Recordset** derived from an e-mail data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="d2c0b-109">Для **записи** на основе, что **записей** будут иметь те же поля.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="d2c0b-110">Тем не менее эту **запись** также может содержать другие поля уникальный конкретное сообщение, представленный этой **записи**, такие как вложение и Cc (копия).</span><span class="sxs-lookup"><span data-stu-id="d2c0b-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="d2c0b-111">Несмотря на то, что объект **записи** и текущей строки **набора записей** имеют те же поля, они отличаются, поскольку **записей** и **записи** у каждого объекта есть различные методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="d2c0b-112">Поле Общее удерживаемых **записей** и **записи** может быть изменено на любой из этих объектов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-112">A field held in common by the **Record** and **Recordset** can be modified on either object.</span></span> <span data-ttu-id="d2c0b-113">Тем не менее, невозможно удалить поле на объект **записи** , несмотря на то, что основной поставщик может поддерживать Установка поля значения null.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-113">However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="d2c0b-114">После открытия **записи** можно программными средствами добавить поля.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-114">After the **Record** is opened, you can programmatically add fields.</span></span> <span data-ttu-id="d2c0b-115">Также можно удалить поля, которые были добавлены, но не смогут удалять поля из исходного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-115">You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="d2c0b-116">Кроме того, может открыть объект **записи** непосредственно из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-116">You may also open the **Record** object directly from a URL.</span></span> <span data-ttu-id="d2c0b-117">В этом случае поля, добавляемые к **записи** зависят от базового поставщика.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-117">In this case, the fields added to the **Record** depend on the underlying provider.</span></span> <span data-ttu-id="d2c0b-118">На данный момент большинство поставщиков добавьте набор полей, которые описывают сущности, представленной **записи**.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-118">Currently, most providers add a set of fields that describe the entity represented by the **Record**.</span></span> <span data-ttu-id="d2c0b-119">Если сущность состоит из потока в байтах, такие как простой файл, затем объект [потока](stream-object-ado.md) обычно могут быть открыты из **записи**.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-119">If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="d2c0b-120">Особых полей для документа источника поставщиков</span><span class="sxs-lookup"><span data-stu-id="d2c0b-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="d2c0b-121">Специальный класс поставщиков, *поставщики источников документов*управляет папки и документы.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-121">A special class of providers, called *document source providers*, manages folders and documents.</span></span> <span data-ttu-id="d2c0b-122">Когда объект **записи** представляет документ, или объекта **набора записей** представляет папку документов, поставщик источника документов заполняет объектам с уникальный набор полей, описывающих характеристики документа, а не Фактические сам документ.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-122">When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</span></span> <span data-ttu-id="d2c0b-123">Как правило одно поле содержит ссылку на **поток** , представляющий документ.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-123">Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="d2c0b-124">Эти поля составляют ресурса **записи** или **набора записей** и перечислены для конкретных поставщиков, которые поддерживают их в [Приложении A: поставщиков](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="d2c0b-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="d2c0b-125">Две константы индексирования коллекции **полей** ресурса **запись** или **набор записей** для получения пары часто используемых полей.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-125">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields.</span></span> <span data-ttu-id="d2c0b-126">Свойство [Value](value-property-ado.md) объекта **поля** возвращает нужное содержимое.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-126">The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="d2c0b-127">В поле получить доступ с константой **adDefaultStream** содержится поток по умолчанию, связанного с объектом **набора записей** или **записи** .</span><span class="sxs-lookup"><span data-stu-id="d2c0b-127">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object.</span></span> <span data-ttu-id="d2c0b-128">Поставщик назначает поток по умолчанию для объекта.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-128">The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="d2c0b-129">В поле получить доступ с константой **adRecordURL** содержится абсолютный URL-адрес для идентификации документа.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="d2c0b-130">Поставщик источника документов не поддерживает набор [свойств](properties-collection-ado.md) объектов **записи** и **поля** .</span><span class="sxs-lookup"><span data-stu-id="d2c0b-130">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects.</span></span> <span data-ttu-id="d2c0b-131">Содержимое коллекции **свойств** имеет значение null для таких объектов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-131">The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="d2c0b-132">Поставщик источника документов могут добавлять свойства от поставщика, например **Тип источника данных** , чтобы определить, является ли поставщик источника документа.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-132">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider.</span></span> <span data-ttu-id="d2c0b-133">Дополнительные сведения об определении типа поставщика, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-133">For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="d2c0b-134">Столбцы набора записей ресурсов</span><span class="sxs-lookup"><span data-stu-id="d2c0b-134">Resource Recordset Columns</span></span>

<span data-ttu-id="d2c0b-135">*Набор записей ресурсов* состоит из следующих столбцов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2c0b-136">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="d2c0b-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="d2c0b-137">Тип</span><span class="sxs-lookup"><span data-stu-id="d2c0b-137">Type</span></span></p></th>
<th><p><span data-ttu-id="d2c0b-138">Описание</span><span class="sxs-lookup"><span data-stu-id="d2c0b-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-141">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-141">Read-only.</span></span> <span data-ttu-id="d2c0b-142">Указывает URL-адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-142">Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-145">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-145">Read-only.</span></span> <span data-ttu-id="d2c0b-146">Указывает абсолютный URL-адрес родительской записи.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-146">Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-149">Read-only.</span></span> <span data-ttu-id="d2c0b-150">Указывает абсолютный URL-адрес ресурса, который является объединение здесь и PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-150">Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="d2c0b-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="d2c0b-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-153">Значение true, если скрыта ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-153">True if the resource is hidden.</span></span> <span data-ttu-id="d2c0b-154">Строки не будут возвращены, если команда, который создает набор строк явным образом выбирает строк, где RESOURCE_ISHIDDEN имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-154">No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="d2c0b-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="d2c0b-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-157">Значение true, если ресурс доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-157">True if the resource is read-only.</span></span> <span data-ttu-id="d2c0b-158">Не удалось открыть этот ресурс с DBBINDFLAG_WRITE и будет с DB_E_READONLY.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-158">Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</span></span> <span data-ttu-id="d2c0b-159">Это свойство может быть изменен, даже если ресурс был открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-159">This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="d2c0b-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-162">Указывает на использование скорее всего документа — например, юрист краткое.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="d2c0b-163">Это может соответствовать шаблонов Office, используемые для создания документа.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="d2c0b-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="d2c0b-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-166">Указывает тип MIME документа, например, указывающее формат &quot;text/html&quot;. "</span><span class="sxs-lookup"><span data-stu-id="d2c0b-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="d2c0b-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-169">Указывает язык, в котором будет храниться содержимое.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="d2c0b-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-172">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-172">Read-only.</span></span> <span data-ttu-id="d2c0b-173">Указывает на структуру FILETIME, содержащую время создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-173">Indicates a FILETIME structure containing the time the resource was created.</span></span> <span data-ttu-id="d2c0b-174">Время отображается в формате по Гринвичу (UTC).</span><span class="sxs-lookup"><span data-stu-id="d2c0b-174">The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="d2c0b-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-177">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-177">Read-only.</span></span> <span data-ttu-id="d2c0b-178">Указывает на структуру FILETIME, содержащую время последнего обращения к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-178">Indicates a FILETIME structure containing the time that the resource was last accessed.</span></span> <span data-ttu-id="d2c0b-179">— Это время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-179">The time is in UTC format.</span></span> <span data-ttu-id="d2c0b-180">Члены FILETIME, нулю, если поставщик не поддерживает этот элемент времени.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-180">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="d2c0b-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-183">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-183">Read-only.</span></span> <span data-ttu-id="d2c0b-184">Указывает на структуру FILETIME, содержащую время последней операции записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-184">Indicates a FILETIME structure containing the time that the resource was last written.</span></span> <span data-ttu-id="d2c0b-185">— Это время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-185">The time is in UTC format.</span></span> <span data-ttu-id="d2c0b-186">Члены FILETIME, нулю, если поставщик не поддерживает этот элемент времени.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-186">The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="d2c0b-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="d2c0b-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-189">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-189">Read-only.</span></span> <span data-ttu-id="d2c0b-190">Указывает размер потока ресурсов по умолчанию, в байтах.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-190">Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="d2c0b-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="d2c0b-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-193">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-193">Read-only.</span></span> <span data-ttu-id="d2c0b-194">Значение true, если ресурса семейства сайтов, таких как каталог.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-194">True if the resource is a collection, such as a directory.</span></span> <span data-ttu-id="d2c0b-195">False, если ресурс является простой файл.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-195">False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="d2c0b-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="d2c0b-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-198">Значение true, если ресурса структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-198">True if the resource is a structured document.</span></span> <span data-ttu-id="d2c0b-199">False, если ресурс не структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-199">False if the resource is not a structured document.</span></span> <span data-ttu-id="d2c0b-200">Это может быть коллекцию или простой файл.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-200">It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="d2c0b-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-203">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-203">Read-only.</span></span> <span data-ttu-id="d2c0b-204">Указывает, что этот ресурс содержит URL-адрес для простой документ по умолчанию, папки или структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-204">Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</span></span> <span data-ttu-id="d2c0b-205">Используется при запросе поток по умолчанию из ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-205">Used when the default stream is requested from a resource.</span></span> <span data-ttu-id="d2c0b-206">Это свойство не задан для простого файла.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-206">This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="d2c0b-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="d2c0b-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-209">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-209">Read-only.</span></span> <span data-ttu-id="d2c0b-210">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-210">Optional.</span></span> <span data-ttu-id="d2c0b-211">Указывает, главы из строк, которые содержат дочерние элементы ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-211">Indicates the chapter of the rowset containing the children of the resource.</span></span> <span data-ttu-id="d2c0b-212">( <em>Поставщик OLE DB для публикации Интернет</em> не использует этот столбец.)</span><span class="sxs-lookup"><span data-stu-id="d2c0b-212">(The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c0b-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="d2c0b-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="d2c0b-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-215">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-215">Read-only.</span></span> <span data-ttu-id="d2c0b-216">Указывает отображаемое имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-216">Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c0b-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="d2c0b-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="d2c0b-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="d2c0b-219">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-219">Read-only.</span></span> <span data-ttu-id="d2c0b-220">Значение true, если ресурс является корневым каталогом семейства сайтов или структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-220">True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>


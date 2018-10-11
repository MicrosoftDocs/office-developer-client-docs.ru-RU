---
title: Append Method (ADO)
TOCTitle: Append Method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b47b7b0514b78a89425e47962c36b092e35677ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481974"
---
# <a name="append-method-ado"></a><span data-ttu-id="8131e-102">Append Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="8131e-102">Append Method (ADO)</span></span>


<span data-ttu-id="8131e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8131e-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="8131e-104">Добавляет объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8131e-104">Appends an object to a collection.</span></span> <span data-ttu-id="8131e-105">Если семейство [полей](fields-collection-ado.md), могут быть созданы новый объект [поля](field-object-ado.md) перед добавлением в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8131e-105">If the collection is [Fields](fields-collection-ado.md), a new [Field](field-object-ado.md) object may be created before it is appended to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8131e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8131e-106">Syntax</span></span>

<span data-ttu-id="8131e-107">*семейства сайтов*. Добавьте *объект*</span><span class="sxs-lookup"><span data-stu-id="8131e-107">*collection*.Append *object*</span></span>

<span data-ttu-id="8131e-108">*поля*. Добавьте *имя*, *Тип*, *DefinedSize*, *атрибуты*, *FieldValue*</span><span class="sxs-lookup"><span data-stu-id="8131e-108">*fields*.Append *Name*, *Type*, *DefinedSize*, *Attrib*, *FieldValue*</span></span>

## <a name="parameters"></a><span data-ttu-id="8131e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8131e-109">Parameters</span></span>

  - <span data-ttu-id="8131e-110">*семейства сайтов*</span><span class="sxs-lookup"><span data-stu-id="8131e-110">*collection*</span></span>

  - <span data-ttu-id="8131e-111">Объект collection.</span><span class="sxs-lookup"><span data-stu-id="8131e-111">A collection object.</span></span>

  - <span data-ttu-id="8131e-112">*fields*</span><span class="sxs-lookup"><span data-stu-id="8131e-112">*fields*</span></span>

  - <span data-ttu-id="8131e-113">Коллекция **полей** .</span><span class="sxs-lookup"><span data-stu-id="8131e-113">A **Fields** collection.</span></span>

  - <span data-ttu-id="8131e-114">*object*</span><span class="sxs-lookup"><span data-stu-id="8131e-114">*object*</span></span>

  - <span data-ttu-id="8131e-115">Объектная переменная, представляющий объект, который будет добавляться.</span><span class="sxs-lookup"><span data-stu-id="8131e-115">An object variable that represents the object to be appended.</span></span>

  - <span data-ttu-id="8131e-116">*Name*</span><span class="sxs-lookup"><span data-stu-id="8131e-116">*Name*</span></span>

  - <span data-ttu-id="8131e-117">**Строковое** значение, которое содержит имя новый объект **поля** , а не должны быть одинаковыми имя как любой другой объект в *полях*.</span><span class="sxs-lookup"><span data-stu-id="8131e-117">A **String** value that contains the name of the new **Field** object, and must not be the same name as any other object in *fields*.</span></span>

  - <span data-ttu-id="8131e-118">*Тип*</span><span class="sxs-lookup"><span data-stu-id="8131e-118">*Type*</span></span>

  - <span data-ttu-id="8131e-119">Значение [DataTypeEnum](datatypeenum.md) , чье значение по умолчанию — это **adEmpty**, определяющее тип данных нового поля.</span><span class="sxs-lookup"><span data-stu-id="8131e-119">A [DataTypeEnum](datatypeenum.md) value, whose default value is **adEmpty**, that specifies the data type of the new field.</span></span> <span data-ttu-id="8131e-120">Следующие типы данных не поддерживаются ADO и должны не будет использоваться при добавления новых полей **набора записей**: **adIDispatch**, **adIUnknown**, **adVariant**.</span><span class="sxs-lookup"><span data-stu-id="8131e-120">The following data types are not supported by ADO, and should not be used when appending new fields to a **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span></span>

  - <span data-ttu-id="8131e-121">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="8131e-121">*DefinedSize*</span></span>

  - <span data-ttu-id="8131e-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8131e-122">Optional.</span></span> <span data-ttu-id="8131e-123">**Длинное** значение, представляющее определенный размер, в байтах нового поля или символов.</span><span class="sxs-lookup"><span data-stu-id="8131e-123">A **Long** value that represents the defined size, in characters or bytes, of the new field.</span></span> <span data-ttu-id="8131e-124">Значение по умолчанию для этого параметра является производным от *типа*.</span><span class="sxs-lookup"><span data-stu-id="8131e-124">The default value for this parameter is derived from *Type*.</span></span> <span data-ttu-id="8131e-125">Поля со DefinedSize больше, чем 255 байт и обрабатываются как столбцы переменной длины.</span><span class="sxs-lookup"><span data-stu-id="8131e-125">Fields with a DefinedSize greater than 255 bytes, and treated as variable length columns.</span></span> <span data-ttu-id="8131e-126">(По умолчанию *DefinedSize* не определено.)</span><span class="sxs-lookup"><span data-stu-id="8131e-126">(The default *DefinedSize* is unspecified.)</span></span>

  - <span data-ttu-id="8131e-127">*Атрибуты*</span><span class="sxs-lookup"><span data-stu-id="8131e-127">*Attrib*</span></span>

  - <span data-ttu-id="8131e-128">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8131e-128">Optional.</span></span> <span data-ttu-id="8131e-129">Значение [FieldAttributeEnum](fieldattributeenum.md) , чье значение по умолчанию — это **adFldDefault**, который определяет атрибуты для нового поля.</span><span class="sxs-lookup"><span data-stu-id="8131e-129">A [FieldAttributeEnum](fieldattributeenum.md) value, whose default value is **adFldDefault**, that specifies attributes for the new field.</span></span> <span data-ttu-id="8131e-130">Если это значение не указан, поле будет содержать атрибуты, производные от *типа*.</span><span class="sxs-lookup"><span data-stu-id="8131e-130">If this value is not specified, the field will contain attributes derived from *Type*.</span></span>

  - <span data-ttu-id="8131e-131">*FieldValue*</span><span class="sxs-lookup"><span data-stu-id="8131e-131">*FieldValue*</span></span>

  - <span data-ttu-id="8131e-132">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8131e-132">Optional.</span></span> <span data-ttu-id="8131e-133">**Variant** , который представляет значение для нового поля.</span><span class="sxs-lookup"><span data-stu-id="8131e-133">A **Variant** that represents the value for the new field.</span></span> <span data-ttu-id="8131e-134">Если не указан, то поле добавляется нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8131e-134">If not specified, then the field is appended with a null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8131e-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="8131e-135">Remarks</span></span>

<span data-ttu-id="8131e-136">**Коллекция параметров**</span><span class="sxs-lookup"><span data-stu-id="8131e-136">**Parameters Collection**</span></span>

<span data-ttu-id="8131e-137">Перед добавлением в коллекцию **параметров** , необходимо установить свойство [типа](type-property-ado.md) объекта [параметров](parameter-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8131e-137">You must set the [Type](type-property-ado.md) property of a [Parameter](parameter-object-ado.md) object before appending it to the **Parameters** collection.</span></span> <span data-ttu-id="8131e-138">Если выбран тип данных переменной длины, вам необходимо также установить свойство [Size](size-property-ado.md) значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="8131e-138">If you select a variable-length data type, you must also set the [Size](size-property-ado.md) property to a value greater than zero.</span></span>

<span data-ttu-id="8131e-139">Описание параметров самостоятельно минимизирует вызовы к поставщику и поэтому улучшает производительность при использовании хранимых процедур или параметризованные запросы.</span><span class="sxs-lookup"><span data-stu-id="8131e-139">Describing parameters yourself minimizes calls to the provider and consequently improves performance when using stored procedures or parameterized queries.</span></span> <span data-ttu-id="8131e-140">Тем не менее необходимо знать свойства параметров, связанных с хранимую процедуру или параметризованный запрос, который требуется позвонить.</span><span class="sxs-lookup"><span data-stu-id="8131e-140">However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</span></span>

<span data-ttu-id="8131e-141">Метод [CreateParameter](createparameter-method-ado.md) используется для создания объектов **параметров** с соответствующими параметрами свойств и метод **Append** используется для добавления их в коллекцию [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8131e-141">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the **Append** method to add them to the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="8131e-142">Это позволяет задать и возвращаемые значения параметра без вызова поставщика для получения параметров.</span><span class="sxs-lookup"><span data-stu-id="8131e-142">This lets you set and return parameter values without having to call the provider for the parameter information.</span></span> <span data-ttu-id="8131e-143">При создании поставщика, который не предоставляет сведений о параметрах необходимо использовать этот метод для вручную заполнить коллекцию **параметров** для использования на всех параметров.</span><span class="sxs-lookup"><span data-stu-id="8131e-143">If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the **Parameters** collection in order to use parameters at all.</span></span>

<span data-ttu-id="8131e-144">**Коллекции полей**</span><span class="sxs-lookup"><span data-stu-id="8131e-144">**Fields Collection**</span></span>

<span data-ttu-id="8131e-145">Параметр *FieldValue* действителен только в том случае, при добавлении объекта **поля** объект [записи](record-object-ado.md) , а не для объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8131e-145">The *FieldValue* parameter is only valid when adding a **Field** object to a [Record](record-object-ado.md) object, not to a **Recordset** object.</span></span> <span data-ttu-id="8131e-146">С объектом **записи** можно добавить поля и указывать значения в то же время.</span><span class="sxs-lookup"><span data-stu-id="8131e-146">With a **Record** object, you may append fields and provide values at the same time.</span></span> <span data-ttu-id="8131e-147">С объектом **набора записей** необходимо создать поля закрытой **набора записей** , затем открыть **записей** и назначить значения поля.</span><span class="sxs-lookup"><span data-stu-id="8131e-147">With a **Recordset** object, you must create fields while the **Recordset** is closed, then open the **Recordset** and assign values to the fields.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8131e-148">Для нового <STRONG>поля</STRONG> объектов, к коллекции <STRONG>полей</STRONG> объекта <STRONG>записи</STRONG> свойство <A href="value-property-ado.md">Value</A> необходимо установить перед можно указать любые другие свойства <STRONG>поля</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8131e-148">For new <STRONG>Field</STRONG> objects that have been appended to the <STRONG>Fields</STRONG> collection of a <STRONG>Record</STRONG> object, the <A href="value-property-ado.md">Value</A> property must be set before any other <STRONG>Field</STRONG> properties can be specified.</span></span> <span data-ttu-id="8131e-149">Во-первых определенного значения для свойства <STRONG>Value</STRONG> должна быть назначена и вызове <A href="update-method-ado.md">Update</A> в коллекции <STRONG>полей</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8131e-149">First, a specific value for the <STRONG>Value</STRONG> property must have been assigned and <A href="update-method-ado.md">Update</A> on the <STRONG>Fields</STRONG> collection called.</span></span> <span data-ttu-id="8131e-150">Затем осуществляется другие свойства, такие как <A href="type-property-ado.md">Тип</A> или <A href="attributes-property-ado.md">атрибуты</A> .</span><span class="sxs-lookup"><span data-stu-id="8131e-150">Then, other properties such as <A href="type-property-ado.md">Type</A> or <A href="attributes-property-ado.md">Attributes</A> can be accessed.</span></span></P>



<span data-ttu-id="8131e-151">Объекты **поля** из следующих типов данных (**DataTypeEnum**) не может быть добавлен к коллекции **полей** и приведет к возникновению ошибки: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**и \*\* adUserDefined\*\*.</span><span class="sxs-lookup"><span data-stu-id="8131e-151">**Field** objects of the following data types (**DataTypeEnum**) cannot be appended to the **Fields** collection and will cause an error to occur: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**, and **adUserDefined**.</span></span> <span data-ttu-id="8131e-152">Кроме того, следующие типы данных не поддерживаются ADO: **adIDispatch**, **adIUnknown**и **adIVariant**.</span><span class="sxs-lookup"><span data-stu-id="8131e-152">Also, the following data types are not supported by ADO: **adIDispatch**, **adIUnknown**, and **adIVariant**.</span></span> <span data-ttu-id="8131e-153">Для этих типов то ошибки не возникает при добавлении, но использование может привести к непредсказуемым последствиям, включая утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="8131e-153">For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</span></span>

<span data-ttu-id="8131e-154">**Набор записей**</span><span class="sxs-lookup"><span data-stu-id="8131e-154">**Recordset**</span></span>

<span data-ttu-id="8131e-155">Если свойство [CursorLocation](cursorlocation-property-ado.md) не задано до вызова метода **Append** , **CursorLocation** будет иметь значение **adUseClient** (значение [CursorLocationEnum](cursorlocationenum.md) ) автоматически при объекта [набора](recordset-object-ado.md) [ Открыть](open-method-ado-recordset.md) вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="8131e-155">If you do not set the [CursorLocation](cursorlocation-property-ado.md) property before calling the **Append** method, **CursorLocation** will be set to **adUseClient** (a [CursorLocationEnum](cursorlocationenum.md) value) automatically when the [Recordset](recordset-object-ado.md) object's [Open](open-method-ado-recordset.md) method is called.</span></span>

<span data-ttu-id="8131e-156">При вызове метода **Append** коллекцию **полей** open **записей**, либо на **набор записей** , где было установлено свойство [ActiveConnection](activeconnection-property-ado.md) произойдет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="8131e-156">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset**, or on a **Recordset** where the [ActiveConnection](activeconnection-property-ado.md) property has been set.</span></span> <span data-ttu-id="8131e-157">Только добавлением полей **набора записей** , который не был открыт и еще не был подключен к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="8131e-157">You can only append fields to a **Recordset** that is not open and has not yet been connected to a data source.</span></span> <span data-ttu-id="8131e-158">Обычно это регистр при объект **набора записей** с помощью метода [CreateRecordset](createrecordset-method-rds.md) с целью или назначается объектную переменную.</span><span class="sxs-lookup"><span data-stu-id="8131e-158">This is typically the case when a **Recordset** object is fabricated with the [CreateRecordset](createrecordset-method-rds.md) method or assigned to an object variable.</span></span>

<span data-ttu-id="8131e-159">**Запись**</span><span class="sxs-lookup"><span data-stu-id="8131e-159">**Record**</span></span>

<span data-ttu-id="8131e-160">Ошибка во время выполнения не возникает, если для коллекции **полей** open **записи**вызывается метод **Append** .</span><span class="sxs-lookup"><span data-stu-id="8131e-160">A run-time error will not occur if the **Append** method is called on the **Fields** collection of an open **Record**.</span></span> <span data-ttu-id="8131e-161">Новое поле будет добавлен к коллекции **полей** объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="8131e-161">The new field will be added to the **Record** object's **Fields** collection.</span></span> <span data-ttu-id="8131e-162">Если **запись** был получен из **набора записей**, нового поля не отображаются в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8131e-162">If the **Record** was derived from a **Recordset**, then the new field will not appear in the **Recordset** object's **Fields** collection.</span></span>

<span data-ttu-id="8131e-163">Поля несуществующий создаются и добавляются в коллекцию **полей** , назначив значение объекта поля, как если бы он уже существует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8131e-163">A non-existent field can be created and appended to the **Fields** collection by assigning a value to the field object as if it already existed in the collection.</span></span> <span data-ttu-id="8131e-164">Назначение запустит автоматического создания и добавления объекта **поля** , а затем назначения будет завершена.</span><span class="sxs-lookup"><span data-stu-id="8131e-164">The assignment will trigger the automatic creation and appending of the **Field** object, then the assignment will be completed.</span></span>

<span data-ttu-id="8131e-165">После добавления **поля** в коллекцию **полей** объект **записи** , вызовите метод **Update** коллекции **полей** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="8131e-165">After appending a **Field** to a **Record** object's **Fields** collection, call the **Update** method of the **Fields** collection to save the change.</span></span>


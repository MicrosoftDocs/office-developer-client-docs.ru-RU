---
title: Метод Append (ADO)
TOCTitle: Append method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03a953b34932a5090ab40abbc7613e3518506070
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925658"
---
# <a name="append-method-ado"></a><span data-ttu-id="af8dc-102">Метод Append (ADO)</span><span class="sxs-lookup"><span data-stu-id="af8dc-102">Append method (ADO)</span></span>


<span data-ttu-id="af8dc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af8dc-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="af8dc-104">Добавляет объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="af8dc-104">Appends an object to a collection.</span></span> <span data-ttu-id="af8dc-105">Если семейство [полей](fields-collection-ado.md), могут быть созданы новый объект [поля](field-object-ado.md) перед добавлением в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="af8dc-105">If the collection is [Fields](fields-collection-ado.md), a new [Field](field-object-ado.md) object may be created before it is appended to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="af8dc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af8dc-106">Syntax</span></span>

<span data-ttu-id="af8dc-107">*семейства сайтов*. Добавьте *объект*</span><span class="sxs-lookup"><span data-stu-id="af8dc-107">*collection*.Append *object*</span></span>

<span data-ttu-id="af8dc-108">*поля*. Добавьте *имя*, *Тип*, *DefinedSize*, *атрибуты*, *FieldValue*</span><span class="sxs-lookup"><span data-stu-id="af8dc-108">*fields*.Append *Name*, *Type*, *DefinedSize*, *Attrib*, *FieldValue*</span></span>

## <a name="parameters"></a><span data-ttu-id="af8dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af8dc-109">Parameters</span></span>

  - <span data-ttu-id="af8dc-110">*семейства сайтов*</span><span class="sxs-lookup"><span data-stu-id="af8dc-110">*collection*</span></span>

  - <span data-ttu-id="af8dc-111">Объект collection.</span><span class="sxs-lookup"><span data-stu-id="af8dc-111">A collection object.</span></span>

  - <span data-ttu-id="af8dc-112">*fields*</span><span class="sxs-lookup"><span data-stu-id="af8dc-112">*fields*</span></span>

  - <span data-ttu-id="af8dc-113">Коллекция **полей** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-113">A **Fields** collection.</span></span>

  - <span data-ttu-id="af8dc-114">*object*</span><span class="sxs-lookup"><span data-stu-id="af8dc-114">*object*</span></span>

  - <span data-ttu-id="af8dc-115">Объектная переменная, представляющий объект, который будет добавляться.</span><span class="sxs-lookup"><span data-stu-id="af8dc-115">An object variable that represents the object to be appended.</span></span>

  - <span data-ttu-id="af8dc-116">*Name*</span><span class="sxs-lookup"><span data-stu-id="af8dc-116">*Name*</span></span>

  - <span data-ttu-id="af8dc-117">**Строковое** значение, которое содержит имя новый объект **поля** , а не должны быть одинаковыми имя как любой другой объект в *полях*.</span><span class="sxs-lookup"><span data-stu-id="af8dc-117">A **String** value that contains the name of the new **Field** object, and must not be the same name as any other object in *fields*.</span></span>

  - <span data-ttu-id="af8dc-118">*Тип*</span><span class="sxs-lookup"><span data-stu-id="af8dc-118">*Type*</span></span>

  - <span data-ttu-id="af8dc-119">Значение [DataTypeEnum](datatypeenum.md) , чье значение по умолчанию — это **adEmpty**, определяющее тип данных нового поля.</span><span class="sxs-lookup"><span data-stu-id="af8dc-119">A [DataTypeEnum](datatypeenum.md) value, whose default value is **adEmpty**, that specifies the data type of the new field.</span></span> <span data-ttu-id="af8dc-120">Следующие типы данных не поддерживаются ADO и должны не будет использоваться при добавления новых полей **набора записей**: **adIDispatch**, **adIUnknown**, **adVariant**.</span><span class="sxs-lookup"><span data-stu-id="af8dc-120">The following data types are not supported by ADO, and should not be used when appending new fields to a **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span></span>

  - <span data-ttu-id="af8dc-121">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="af8dc-121">*DefinedSize*</span></span>

  - <span data-ttu-id="af8dc-122">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="af8dc-122">Optional.</span></span> <span data-ttu-id="af8dc-123">**Длинное** значение, представляющее определенный размер, в байтах нового поля или символов.</span><span class="sxs-lookup"><span data-stu-id="af8dc-123">A **Long** value that represents the defined size, in characters or bytes, of the new field.</span></span> <span data-ttu-id="af8dc-124">Значение по умолчанию для этого параметра является производным от *типа*.</span><span class="sxs-lookup"><span data-stu-id="af8dc-124">The default value for this parameter is derived from *Type*.</span></span> <span data-ttu-id="af8dc-125">Поля со DefinedSize больше, чем 255 байт и обрабатываются как столбцы переменной длины.</span><span class="sxs-lookup"><span data-stu-id="af8dc-125">Fields with a DefinedSize greater than 255 bytes, and treated as variable length columns.</span></span> <span data-ttu-id="af8dc-126">(По умолчанию *DefinedSize* не определено.)</span><span class="sxs-lookup"><span data-stu-id="af8dc-126">(The default *DefinedSize* is unspecified.)</span></span>

  - <span data-ttu-id="af8dc-127">*Атрибуты*</span><span class="sxs-lookup"><span data-stu-id="af8dc-127">*Attrib*</span></span>

  - <span data-ttu-id="af8dc-128">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="af8dc-128">Optional.</span></span> <span data-ttu-id="af8dc-129">Значение [FieldAttributeEnum](fieldattributeenum.md) , чье значение по умолчанию — это **adFldDefault**, который определяет атрибуты для нового поля.</span><span class="sxs-lookup"><span data-stu-id="af8dc-129">A [FieldAttributeEnum](fieldattributeenum.md) value, whose default value is **adFldDefault**, that specifies attributes for the new field.</span></span> <span data-ttu-id="af8dc-130">Если это значение не указан, поле будет содержать атрибуты, производные от *типа*.</span><span class="sxs-lookup"><span data-stu-id="af8dc-130">If this value is not specified, the field will contain attributes derived from *Type*.</span></span>

  - <span data-ttu-id="af8dc-131">*FieldValue*</span><span class="sxs-lookup"><span data-stu-id="af8dc-131">*FieldValue*</span></span>

  - <span data-ttu-id="af8dc-132">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="af8dc-132">Optional.</span></span> <span data-ttu-id="af8dc-133">**Variant** , который представляет значение для нового поля.</span><span class="sxs-lookup"><span data-stu-id="af8dc-133">A **Variant** that represents the value for the new field.</span></span> <span data-ttu-id="af8dc-134">Если не указан, то поле добавляется нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="af8dc-134">If not specified, then the field is appended with a null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af8dc-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="af8dc-135">Remarks</span></span>

<span data-ttu-id="af8dc-136">**Коллекция параметров**</span><span class="sxs-lookup"><span data-stu-id="af8dc-136">**Parameters Collection**</span></span>

<span data-ttu-id="af8dc-137">Перед добавлением в коллекцию **параметров** , необходимо установить свойство [типа](type-property-ado.md) объекта [параметров](parameter-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="af8dc-137">You must set the [Type](type-property-ado.md) property of a [Parameter](parameter-object-ado.md) object before appending it to the **Parameters** collection.</span></span> <span data-ttu-id="af8dc-138">Если выбран тип данных переменной длины, вам необходимо также установить свойство [Size](size-property-ado.md) значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="af8dc-138">If you select a variable-length data type, you must also set the [Size](size-property-ado.md) property to a value greater than zero.</span></span>

<span data-ttu-id="af8dc-139">Описание параметров самостоятельно минимизирует вызовы к поставщику и поэтому улучшает производительность при использовании хранимых процедур или параметризованные запросы.</span><span class="sxs-lookup"><span data-stu-id="af8dc-139">Describing parameters yourself minimizes calls to the provider and consequently improves performance when using stored procedures or parameterized queries.</span></span> <span data-ttu-id="af8dc-140">Тем не менее необходимо знать свойства параметров, связанных с хранимую процедуру или параметризованный запрос, который требуется позвонить.</span><span class="sxs-lookup"><span data-stu-id="af8dc-140">However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</span></span>

<span data-ttu-id="af8dc-141">Метод [CreateParameter](createparameter-method-ado.md) используется для создания объектов **параметров** с соответствующими параметрами свойств и метод **Append** используется для добавления их в коллекцию [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="af8dc-141">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the **Append** method to add them to the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="af8dc-142">Это позволяет задать и возвращаемые значения параметра без вызова поставщика для получения параметров.</span><span class="sxs-lookup"><span data-stu-id="af8dc-142">This lets you set and return parameter values without having to call the provider for the parameter information.</span></span> <span data-ttu-id="af8dc-143">При создании поставщика, который не предоставляет сведений о параметрах необходимо использовать этот метод для вручную заполнить коллекцию **параметров** для использования на всех параметров.</span><span class="sxs-lookup"><span data-stu-id="af8dc-143">If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the **Parameters** collection in order to use parameters at all.</span></span>

<span data-ttu-id="af8dc-144">**Коллекции полей**</span><span class="sxs-lookup"><span data-stu-id="af8dc-144">**Fields Collection**</span></span>

<span data-ttu-id="af8dc-145">Параметр *FieldValue* действителен только в том случае, при добавлении объекта **поля** объект [записи](record-object-ado.md) , а не для объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-145">The *FieldValue* parameter is only valid when adding a **Field** object to a [Record](record-object-ado.md) object, not to a **Recordset** object.</span></span> <span data-ttu-id="af8dc-146">С объектом **записи** можно добавить поля и указывать значения в то же время.</span><span class="sxs-lookup"><span data-stu-id="af8dc-146">With a **Record** object, you may append fields and provide values at the same time.</span></span> <span data-ttu-id="af8dc-147">С объектом **набора записей** необходимо создать поля закрытой **набора записей** , затем открыть **записей** и назначить значения поля.</span><span class="sxs-lookup"><span data-stu-id="af8dc-147">With a **Recordset** object, you must create fields while the **Recordset** is closed, then open the **Recordset** and assign values to the fields.</span></span>


> [!NOTE]
> <span data-ttu-id="af8dc-148">Для нового **поля** объектов, к коллекции **полей** объекта **записи** свойство [Value](value-property-ado.md) необходимо установить перед можно указать любые другие свойства **поля** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-148">For new **Field** objects that have been appended to the **Fields** collection of a **Record** object, the [Value](value-property-ado.md) property must be set before any other **Field** properties can be specified.</span></span> <span data-ttu-id="af8dc-149">Во-первых определенного значения для свойства **Value** должна быть назначена и вызове [Update](update-method-ado.md) в коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-149">First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called.</span></span> <span data-ttu-id="af8dc-150">Затем осуществляется другие свойства, такие как [Тип](type-property-ado.md) или [атрибуты](attributes-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="af8dc-150">Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>


<span data-ttu-id="af8dc-151">Объекты **поля** из следующих типов данных (**DataTypeEnum**) не может быть добавлен к коллекции **полей** и приведет к возникновению ошибки: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**и \*\* adUserDefined\*\*.</span><span class="sxs-lookup"><span data-stu-id="af8dc-151">**Field** objects of the following data types (**DataTypeEnum**) cannot be appended to the **Fields** collection and will cause an error to occur: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**, and **adUserDefined**.</span></span> <span data-ttu-id="af8dc-152">Кроме того, следующие типы данных не поддерживаются ADO: **adIDispatch**, **adIUnknown**и **adIVariant**.</span><span class="sxs-lookup"><span data-stu-id="af8dc-152">Also, the following data types are not supported by ADO: **adIDispatch**, **adIUnknown**, and **adIVariant**.</span></span> <span data-ttu-id="af8dc-153">Для этих типов то ошибки не возникает при добавлении, но использование может привести к непредсказуемым последствиям, включая утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="af8dc-153">For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</span></span>

<span data-ttu-id="af8dc-154">**Набор записей**</span><span class="sxs-lookup"><span data-stu-id="af8dc-154">**Recordset**</span></span>

<span data-ttu-id="af8dc-155">Если свойство [CursorLocation](cursorlocation-property-ado.md) не задано до вызова метода **Append** , **CursorLocation** будет иметь значение **adUseClient** (значение [CursorLocationEnum](cursorlocationenum.md) ) автоматически при объекта [набора](recordset-object-ado.md) [ Открыть](open-method-ado-recordset.md) вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="af8dc-155">If you do not set the [CursorLocation](cursorlocation-property-ado.md) property before calling the **Append** method, **CursorLocation** will be set to **adUseClient** (a [CursorLocationEnum](cursorlocationenum.md) value) automatically when the [Recordset](recordset-object-ado.md) object's [Open](open-method-ado-recordset.md) method is called.</span></span>

<span data-ttu-id="af8dc-156">При вызове метода **Append** коллекцию **полей** open **записей**, либо на **набор записей** , где было установлено свойство [ActiveConnection](activeconnection-property-ado.md) произойдет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="af8dc-156">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset**, or on a **Recordset** where the [ActiveConnection](activeconnection-property-ado.md) property has been set.</span></span> <span data-ttu-id="af8dc-157">Только добавлением полей **набора записей** , который не был открыт и еще не был подключен к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="af8dc-157">You can only append fields to a **Recordset** that is not open and has not yet been connected to a data source.</span></span> <span data-ttu-id="af8dc-158">Обычно это регистр при объект **набора записей** с помощью метода [CreateRecordset](createrecordset-method-rds.md) с целью или назначается объектную переменную.</span><span class="sxs-lookup"><span data-stu-id="af8dc-158">This is typically the case when a **Recordset** object is fabricated with the [CreateRecordset](createrecordset-method-rds.md) method or assigned to an object variable.</span></span>

<span data-ttu-id="af8dc-159">**Запись**</span><span class="sxs-lookup"><span data-stu-id="af8dc-159">**Record**</span></span>

<span data-ttu-id="af8dc-160">Ошибка во время выполнения не возникает, если для коллекции **полей** open **записи**вызывается метод **Append** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-160">A run-time error will not occur if the **Append** method is called on the **Fields** collection of an open **Record**.</span></span> <span data-ttu-id="af8dc-161">Новое поле будет добавлен к коллекции **полей** объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-161">The new field will be added to the **Record** object's **Fields** collection.</span></span> <span data-ttu-id="af8dc-162">Если **запись** был получен из **набора записей**, нового поля не отображаются в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-162">If the **Record** was derived from a **Recordset**, then the new field will not appear in the **Recordset** object's **Fields** collection.</span></span>

<span data-ttu-id="af8dc-163">Поля несуществующий создаются и добавляются в коллекцию **полей** , назначив значение объекта поля, как если бы он уже существует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="af8dc-163">A non-existent field can be created and appended to the **Fields** collection by assigning a value to the field object as if it already existed in the collection.</span></span> <span data-ttu-id="af8dc-164">Назначение запустит автоматического создания и добавления объекта **поля** , а затем назначения будет завершена.</span><span class="sxs-lookup"><span data-stu-id="af8dc-164">The assignment will trigger the automatic creation and appending of the **Field** object, then the assignment will be completed.</span></span>

<span data-ttu-id="af8dc-165">После добавления **поля** в коллекцию **полей** объект **записи** , вызовите метод **Update** коллекции **полей** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="af8dc-165">After appending a **Field** to a **Record** object's **Fields** collection, call the **Update** method of the **Fields** collection to save the change.</span></span>


---
title: Метод обновления (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306239"
---
# <a name="update-method-ado"></a><span data-ttu-id="97618-102">Метод обновления (ADO)</span><span class="sxs-lookup"><span data-stu-id="97618-102">Update method (ADO)</span></span>

<span data-ttu-id="97618-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97618-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97618-104">Сохраняет все изменения, внесенные в текущую строку объекта [Recordset](recordset-object-ado.md) или коллекцию [Полей](fields-collection-ado.md) объекта [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="97618-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97618-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97618-105">Syntax</span></span>

<span data-ttu-id="97618-106">*набор записей.* Поля *обновления*, *значения*</span><span class="sxs-lookup"><span data-stu-id="97618-106">*recordset*.Update *Fields*, *Values*</span></span>

<span data-ttu-id="97618-107">*запись*.</span><span class="sxs-lookup"><span data-stu-id="97618-107">*record*.</span></span> <span data-ttu-id="97618-108">*Поля*. Обновление</span><span class="sxs-lookup"><span data-stu-id="97618-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="97618-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="97618-109">Parameters</span></span>

|<span data-ttu-id="97618-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="97618-110">Parameter</span></span>|<span data-ttu-id="97618-111">Описание</span><span class="sxs-lookup"><span data-stu-id="97618-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="97618-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="97618-112">*Fields*</span></span> |<span data-ttu-id="97618-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="97618-113">Optional.</span></span> <span data-ttu-id="97618-114">**Вариант,** который представляет одно имя, или массив **Variant,** который представляет имена или расположение полей или полей, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="97618-114">A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="97618-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="97618-115">*Values*</span></span> |<span data-ttu-id="97618-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="97618-116">Optional.</span></span> <span data-ttu-id="97618-117">**Вариант,** который представляет единое значение, или массив **Variant,** который представляет значения для поля или полей в новой записи.</span><span class="sxs-lookup"><span data-stu-id="97618-117">A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="97618-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="97618-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="97618-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="97618-119">Recordset</span></span>

<span data-ttu-id="97618-120">Используйте метод **Update,** чтобы сохранить все изменения, внесенные в текущую запись объекта **Recordset** после вызова метода [AddNew](addnew-method-ado.md) или после изменения каких-либо значений поля в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="97618-120">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record.</span></span> <span data-ttu-id="97618-121">Объект **Recordset** должен поддерживать обновления.</span><span class="sxs-lookup"><span data-stu-id="97618-121">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="97618-122">Чтобы установить значения поля, сделайте одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="97618-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="97618-123">Назначение значений свойству [Значение](field-object-ado.md) объекта [Field](value-property-ado.md) и вызов метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="97618-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="97618-124">Передай имя поля и значение в качестве аргументов с вызовом **Update.**</span><span class="sxs-lookup"><span data-stu-id="97618-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="97618-125">Передай массив имен полей и массив значений с помощью вызова **Update.**</span><span class="sxs-lookup"><span data-stu-id="97618-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="97618-126">При использовании массивов полей и значений в обоих массивах должно быть одинаковое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="97618-126">When you use arrays of fields and values, there must be an equal number of elements in both arrays.</span></span> <span data-ttu-id="97618-127">Кроме того, порядок имен полей должен соответствовать порядку значений поля.</span><span class="sxs-lookup"><span data-stu-id="97618-127">Also, the order of field names must match the order of field values.</span></span> <span data-ttu-id="97618-128">Если число и порядок полей и значений не совпадают, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="97618-128">If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="97618-129">Если объект **Recordset поддерживает** пакетное обновление, можно кэшировать несколько изменений в одну или несколько записей локально до вызова метода [UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="97618-129">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="97618-130">При редактировании текущей записи или добавлении новой записи при вызове метода **UpdateBatch** ADO будет автоматически вызывать метод Update, чтобы сохранить все ожидающие изменения текущей записи перед передачей пакетных изменений поставщику. </span><span class="sxs-lookup"><span data-stu-id="97618-130">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="97618-131">При переходе из записи, добавляемой или редактируемой перед вызовом метода **Update,** ADO автоматически вызывает **обновление,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="97618-131">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="97618-132">Чтобы отменить изменения, внесенные в текущую запись, или отменить добавленную запись, необходимо вызвать метод [CancelUpdate.](cancelupdate-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="97618-132">You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="97618-133">Текущая запись остается текущей после вызова метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="97618-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="97618-134">Record</span><span class="sxs-lookup"><span data-stu-id="97618-134">Record</span></span>

<span data-ttu-id="97618-135">Метод **Update** завершает добавления, удаления и обновления полей в коллекции [Fields](fields-collection-ado.md) объекта **Record.**</span><span class="sxs-lookup"><span data-stu-id="97618-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="97618-136">Например, поля, удаленные методом **Delete,** сразу же помечены для удаления, но остаются в коллекции.</span><span class="sxs-lookup"><span data-stu-id="97618-136">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection.</span></span> <span data-ttu-id="97618-137">Метод **Update** должен быть вызван для удаления этих полей из коллекции поставщика.</span><span class="sxs-lookup"><span data-stu-id="97618-137">The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>


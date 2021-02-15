---
title: Метод Update (ADO)
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
# <a name="update-method-ado"></a><span data-ttu-id="57fa7-102">Метод Update (ADO)</span><span class="sxs-lookup"><span data-stu-id="57fa7-102">Update method (ADO)</span></span>

<span data-ttu-id="57fa7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57fa7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57fa7-104">Сохраняет все изменения, внесенные в текущую строку объекта [Recordset](recordset-object-ado.md) или коллекцию [Fields](fields-collection-ado.md) объекта [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="57fa7-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fa7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57fa7-105">Syntax</span></span>

<span data-ttu-id="57fa7-106">*recordset*. Поля *обновления*, *значения*</span><span class="sxs-lookup"><span data-stu-id="57fa7-106">*recordset*.Update *Fields*, *Values*</span></span>

<span data-ttu-id="57fa7-107">*record*.</span><span class="sxs-lookup"><span data-stu-id="57fa7-107">*record*.</span></span> <span data-ttu-id="57fa7-108">*Поля*. Обновление</span><span class="sxs-lookup"><span data-stu-id="57fa7-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="57fa7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="57fa7-109">Parameters</span></span>

|<span data-ttu-id="57fa7-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="57fa7-110">Parameter</span></span>|<span data-ttu-id="57fa7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="57fa7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="57fa7-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="57fa7-112">*Fields*</span></span> |<span data-ttu-id="57fa7-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57fa7-113">Optional.</span></span> <span data-ttu-id="57fa7-114">**Вариант,** который представляет одно имя, или массив **Variant,** который представляет имена или порядковые позиции поля или поля, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="57fa7-114">A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="57fa7-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="57fa7-115">*Values*</span></span> |<span data-ttu-id="57fa7-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="57fa7-116">Optional.</span></span> <span data-ttu-id="57fa7-117">**Вариант,** который представляет одно значение, или массив **Variant,** который представляет значения для поля или полей в новой записи.</span><span class="sxs-lookup"><span data-stu-id="57fa7-117">A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="57fa7-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="57fa7-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="57fa7-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="57fa7-119">Recordset</span></span>

<span data-ttu-id="57fa7-120">Используйте метод **Update,** чтобы сохранить все изменения, внесенные в текущую запись объекта **Recordset** после вызова метода [AddNew](addnew-method-ado.md) или после изменения значений полей в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="57fa7-120">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record.</span></span> <span data-ttu-id="57fa7-121">Объект **Recordset** должен поддерживать обновления.</span><span class="sxs-lookup"><span data-stu-id="57fa7-121">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="57fa7-122">Чтобы установить значения полей, сделайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="57fa7-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="57fa7-123">Назначьте значения [свойству Value](field-object-ado.md) объекта [Field](value-property-ado.md) и вызовите **метод Update.**</span><span class="sxs-lookup"><span data-stu-id="57fa7-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="57fa7-124">Передав имя поля и значение в качестве аргументов с помощью **вызова Update.**</span><span class="sxs-lookup"><span data-stu-id="57fa7-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="57fa7-125">Передав массив имен полей и массив значений с помощью вызова **Update.**</span><span class="sxs-lookup"><span data-stu-id="57fa7-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="57fa7-126">При использовании массивов полей и значений в обоих массивах должно быть одинаковое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="57fa7-126">When you use arrays of fields and values, there must be an equal number of elements in both arrays.</span></span> <span data-ttu-id="57fa7-127">Кроме того, порядок имен полей должен соответствовать порядку значений полей.</span><span class="sxs-lookup"><span data-stu-id="57fa7-127">Also, the order of field names must match the order of field values.</span></span> <span data-ttu-id="57fa7-128">Если число и порядок полей и значений не совпадают, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="57fa7-128">If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="57fa7-129">Если объект **Recordset** поддерживает пакетное обновление, можно кэшировать несколько изменений в одной или нескольких записях локально, пока не будет вызываться [метод UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="57fa7-129">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="57fa7-130">Если вы редактируете текущую запись или добавляете новую запись при вызове метода **UpdateBatch,** ADO будет автоматически вызывать метод **Update,** чтобы сохранить все ожидающие изменения текущей записи перед передачей пакетных изменений поставщику.</span><span class="sxs-lookup"><span data-stu-id="57fa7-130">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="57fa7-131">При переходе от добавляемой или редактируемой записи перед вызовом метода **Update** ADO автоматически вызывает **Update,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="57fa7-131">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="57fa7-132">Необходимо вызвать метод [CancelUpdate,](cancelupdate-method-ado.md) если вы хотите отменить изменения, внесенные в текущую запись, или удалить только что добавленную запись.</span><span class="sxs-lookup"><span data-stu-id="57fa7-132">You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="57fa7-133">Текущая запись остается текущей после вызова метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="57fa7-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="57fa7-134">Record</span><span class="sxs-lookup"><span data-stu-id="57fa7-134">Record</span></span>

<span data-ttu-id="57fa7-135">Метод **Update** завершает добавление, удаление и обновление полей в коллекции [Fields](fields-collection-ado.md) объекта **Record.**</span><span class="sxs-lookup"><span data-stu-id="57fa7-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="57fa7-136">Например, поля, удаленные с помощью метода **Delete,** помечаются для немедленного удаления, но остаются в коллекции.</span><span class="sxs-lookup"><span data-stu-id="57fa7-136">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection.</span></span> <span data-ttu-id="57fa7-137">Для **удаления** этих полей из коллекции поставщика необходимо с помощью метода Update.</span><span class="sxs-lookup"><span data-stu-id="57fa7-137">The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>


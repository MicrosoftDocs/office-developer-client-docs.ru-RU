---
title: Метод Update (ADO)
TOCTitle: Update Method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 772602b31f83d2255c9fdf1b08fa41541f5fc4da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884109"
---
# <a name="update-method-ado"></a><span data-ttu-id="c4cca-102">Метод Update (ADO)</span><span class="sxs-lookup"><span data-stu-id="c4cca-102">Update Method (ADO)</span></span>


<span data-ttu-id="c4cca-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4cca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4cca-104">Сохраняет все изменения, внесенные в текущей строки [набора записей](recordset-object-ado.md) объекта или коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c4cca-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4cca-105">Syntax</span></span>

<span data-ttu-id="c4cca-106">*набор записей*. Обновление*поля*, *значения*</span><span class="sxs-lookup"><span data-stu-id="c4cca-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="c4cca-107">*запись*.</span><span class="sxs-lookup"><span data-stu-id="c4cca-107">*record*.</span></span> <span data-ttu-id="c4cca-108">*Поля*. Обновление</span><span class="sxs-lookup"><span data-stu-id="c4cca-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="c4cca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4cca-109">Parameters</span></span>

  - <span data-ttu-id="c4cca-110">*Поля*</span><span class="sxs-lookup"><span data-stu-id="c4cca-110">*Fields*</span></span>

  - <span data-ttu-id="c4cca-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c4cca-111">Optional.</span></span> <span data-ttu-id="c4cca-112">**Variant** , который представляет одно имя, или **Variant** массива, который представляет имена или порядковый номер позиции в поле или поля, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="c4cca-112">A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>

  - <span data-ttu-id="c4cca-113">*Значения*</span><span class="sxs-lookup"><span data-stu-id="c4cca-113">*Values*</span></span>

  - <span data-ttu-id="c4cca-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c4cca-114">Optional.</span></span> <span data-ttu-id="c4cca-115">**Variant** , который представляет одно значение, или **Variant** массива, который представляет значения поля или поля в новую запись.</span><span class="sxs-lookup"><span data-stu-id="c4cca-115">A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4cca-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4cca-116">Remarks</span></span>

<span data-ttu-id="c4cca-117">**Набор записей**</span><span class="sxs-lookup"><span data-stu-id="c4cca-117">**Recordset**</span></span>

<span data-ttu-id="c4cca-118">Используйте метод **Update** , чтобы сохранить все изменения, внесенные в текущую запись объекта **набора записей** с момента вызова метода [AddNew](addnew-method-ado.md) или после изменения значения поля в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="c4cca-118">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record.</span></span> <span data-ttu-id="c4cca-119">Объект **набора записей** должен поддерживать обновлений.</span><span class="sxs-lookup"><span data-stu-id="c4cca-119">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="c4cca-120">Для установки значений полей, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c4cca-120">To set field values, do one of the following:</span></span>

  - <span data-ttu-id="c4cca-121">Присвойте значения для свойства [Value](value-property-ado.md) объекта [поля](field-object-ado.md) и вызовите метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="c4cca-121">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

  - <span data-ttu-id="c4cca-122">Передайте имя поля и значение в качестве аргументов при вызове **Update** .</span><span class="sxs-lookup"><span data-stu-id="c4cca-122">Pass a field name and a value as arguments with the **Update** call.</span></span>

  - <span data-ttu-id="c4cca-123">Передайте массив имена полей и массив значений с помощью вызова **обновления** .</span><span class="sxs-lookup"><span data-stu-id="c4cca-123">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="c4cca-124">При использовании массивов поля и значения, должен быть равен число элементов в обоих массивах.</span><span class="sxs-lookup"><span data-stu-id="c4cca-124">When you use arrays of fields and values, there must be an equal number of elements in both arrays.</span></span> <span data-ttu-id="c4cca-125">Кроме того порядок имена полей должен соответствовать порядке значений полей.</span><span class="sxs-lookup"><span data-stu-id="c4cca-125">Also, the order of field names must match the order of field values.</span></span> <span data-ttu-id="c4cca-126">Если число и порядок полей и их значения не совпадают, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c4cca-126">If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="c4cca-127">Если объект **набора записей** поддерживает пакетного обновления, можно кэшировать внесение нескольких изменений в одну или несколько записей локально до вызова метода [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c4cca-127">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="c4cca-128">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод **Update** для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="c4cca-128">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="c4cca-129">При перемещении из записи добавлении или редактировании до вызова метода **Update** , ADO автоматически вызывает **обновления** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="c4cca-129">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="c4cca-130">Необходимо вызвать метод [CancelUpdate](cancelupdate-method-ado.md) , чтобы отменить все изменения, внесенные в текущую запись или отменить только что добавленный запись.</span><span class="sxs-lookup"><span data-stu-id="c4cca-130">You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="c4cca-131">Текущая запись остается текущей после вызова метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="c4cca-131">The current record remains current after you call the **Update** method.</span></span>

<span data-ttu-id="c4cca-132">**Запись**</span><span class="sxs-lookup"><span data-stu-id="c4cca-132">**Record**</span></span>

<span data-ttu-id="c4cca-133">Метод **Update** завершает добавления, удаления и обновления полей в коллекции [полей](fields-collection-ado.md) объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="c4cca-133">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="c4cca-134">Например поля, удаленных с помощью метода **Delete** помеченным для удаления сразу же, но остаются в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c4cca-134">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection.</span></span> <span data-ttu-id="c4cca-135">Необходимо быть вызван метод **Update** фактически удалить эти поля из коллекции поставщиков.</span><span class="sxs-lookup"><span data-stu-id="c4cca-135">The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>


---
title: Свойство SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709266"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="f3fe2-102">Свойство SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="f3fe2-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="f3fe2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3fe2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3fe2-104">Указывает, какой столбец для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3fe2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3fe2-105">Syntax</span></span>

<span data-ttu-id="f3fe2-106">*DataControl*. SortColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="f3fe2-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="f3fe2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f3fe2-107">Parameters</span></span>

|<span data-ttu-id="f3fe2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f3fe2-108">Parameter</span></span>|<span data-ttu-id="f3fe2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f3fe2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3fe2-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f3fe2-110">*DataControl*</span></span> |<span data-ttu-id="f3fe2-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="f3fe2-112">*String*</span><span class="sxs-lookup"><span data-stu-id="f3fe2-112">*String*</span></span> |<span data-ttu-id="f3fe2-113">**Строковое** значение, представляющее имя или псевдоним столбца, по которому выполняется сортировка записей.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f3fe2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3fe2-114">Remarks</span></span>

<span data-ttu-id="f3fe2-115">**SortColumn**, [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-115">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="f3fe2-116">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="f3fe2-117">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="f3fe2-118">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="f3fe2-119">Для сортировки по **записей**, необходимо предварительно сохранить все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="f3fe2-120">Если вы используете **RDS. DataControl**, можно использовать метод [SubmitChanges](submitchanges-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe2-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="f3fe2-121">Например если ваше **RDS. DataControl** — с именем ADC1, код может быть ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="f3fe2-122">При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe2-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="f3fe2-123">С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe2-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="f3fe2-124">Например, код может быть myRS.UpdateBatch или.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="f3fe2-125">При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe2-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="f3fe2-126">С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fe2-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="f3fe2-127">Например код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


---
title: Свойство SortColumn (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a613ed053bd91685286066bfa534c41b99edbdd1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874757"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="ebdce-102">Свойство SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="ebdce-102">SortColumn Property (RDS)</span></span>


<span data-ttu-id="ebdce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebdce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebdce-104">Указывает, какой столбец для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="ebdce-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebdce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebdce-105">Syntax</span></span>

<span data-ttu-id="ebdce-106">*DataControl*. SortColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="ebdce-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ebdce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebdce-107">Parameters</span></span>

  - <span data-ttu-id="ebdce-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ebdce-108">*DataControl*</span></span>

  - <span data-ttu-id="ebdce-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="ebdce-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="ebdce-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="ebdce-110">*String*</span></span>

  - <span data-ttu-id="ebdce-111">**Строковое** значение, представляющее имя или псевдоним столбца, по которому выполняется сортировка записей.</span><span class="sxs-lookup"><span data-stu-id="ebdce-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebdce-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="ebdce-112">Remarks</span></span>

<span data-ttu-id="ebdce-113">**SortColumn**, [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="ebdce-113">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="ebdce-114">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="ebdce-114">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="ebdce-115">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="ebdce-115">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="ebdce-116">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="ebdce-116">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="ebdce-117">Для сортировки по **записей**, необходимо предварительно сохранить все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="ebdce-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="ebdce-118">Если вы используете **RDS. DataControl**, можно использовать метод [SubmitChanges](submitchanges-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdce-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="ebdce-119">Например если ваше **RDS. DataControl** — с именем ADC1, код может быть ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="ebdce-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="ebdce-120">При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdce-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="ebdce-121">С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdce-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="ebdce-122">Например, код может быть myRS.UpdateBatch или.</span><span class="sxs-lookup"><span data-stu-id="ebdce-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="ebdce-123">При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdce-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="ebdce-124">С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdce-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="ebdce-125">Например код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="ebdce-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


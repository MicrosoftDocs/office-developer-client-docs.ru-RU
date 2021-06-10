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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306890"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="dbb85-102">Свойство SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="dbb85-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="dbb85-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbb85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbb85-104">Указывает, в какой столбце сортировать записи.</span><span class="sxs-lookup"><span data-stu-id="dbb85-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb85-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbb85-105">Syntax</span></span>

<span data-ttu-id="dbb85-106">*DataControl*. SortColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="dbb85-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="dbb85-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbb85-107">Parameters</span></span>

|<span data-ttu-id="dbb85-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="dbb85-108">Parameter</span></span>|<span data-ttu-id="dbb85-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dbb85-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dbb85-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="dbb85-110">*DataControl*</span></span> |<span data-ttu-id="dbb85-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="dbb85-112">*String*</span><span class="sxs-lookup"><span data-stu-id="dbb85-112">*String*</span></span> |<span data-ttu-id="dbb85-113">**Строковая** величина, которая представляет имя или псевдоним столбца для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="dbb85-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dbb85-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbb85-114">Remarks</span></span>

<span data-ttu-id="dbb85-115">Свойства **SortColumn,** [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="dbb85-115">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="dbb85-116">Функция сортировки заказывает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="dbb85-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="dbb85-117">Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше.</span><span class="sxs-lookup"><span data-stu-id="dbb85-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="dbb85-118">Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="dbb85-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="dbb85-119">Чтобы сортировать в **наборе Recordset,** сначала необходимо сохранить все ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="dbb85-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="dbb85-120">Если вы используете **RDS. DataControl**, вы можете использовать [метод SubmitChanges.](submitchanges-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="dbb85-121">Например, если ваш **RDS. DataControl** называется ADC1, код будет ADC1. SubmitChanges .</span><span class="sxs-lookup"><span data-stu-id="dbb85-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="dbb85-122">Если вы используете ADO **Recordset,** вы можете использовать его [метод UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="dbb85-123">Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью [метода CreateRecordset.](createrecordset-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="dbb85-124">Например, код может быть myRS.UpdateBatch или .</span><span class="sxs-lookup"><span data-stu-id="dbb85-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="dbb85-125">Если вы используете ADO **Recordset,** вы можете использовать его [метод UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="dbb85-126">Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью [метода CreateRecordset.](createrecordset-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="dbb85-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="dbb85-127">Например, код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch .</span><span class="sxs-lookup"><span data-stu-id="dbb85-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


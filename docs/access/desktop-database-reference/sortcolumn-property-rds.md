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
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="40839-102">Свойство SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="40839-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="40839-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40839-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40839-104">Указывает, по какому столбцу следует отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="40839-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="40839-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40839-105">Syntax</span></span>

<span data-ttu-id="40839-106">*Элемент управления*. SortColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="40839-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="40839-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40839-107">Parameters</span></span>

|<span data-ttu-id="40839-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="40839-108">Parameter</span></span>|<span data-ttu-id="40839-109">Описание</span><span class="sxs-lookup"><span data-stu-id="40839-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="40839-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="40839-110">*DataControl*</span></span> |<span data-ttu-id="40839-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="40839-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="40839-112">*String*</span><span class="sxs-lookup"><span data-stu-id="40839-112">*String*</span></span> |<span data-ttu-id="40839-113">**Строковое** значение, представляющее имя или псевдоним столбца, по которому сортируются записи.</span><span class="sxs-lookup"><span data-stu-id="40839-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="40839-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="40839-114">Remarks</span></span>

<span data-ttu-id="40839-115">Свойства **sortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="40839-115">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="40839-116">Функция сортировки упорядочивает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="40839-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="40839-117">Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="40839-118">Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** записей на обновляемый. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="40839-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="40839-119">Для сортировки по **набору записей**сначала необходимо сохранить все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="40839-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="40839-120">Если вы используете **RDS. Элемент управления**, вы можете использовать метод [SubmitChanges](submitchanges-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="40839-121">Например, если вы **RDS. Элемент управления** ADC1 с именем, код будет ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="40839-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="40839-122">Если вы используете **набор записей**ADO, вы можете использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="40839-123">Использование **UpdateBatch** является рекомендуемым методом для объектов **Recordset** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="40839-124">Например, ваш код может быть Мирс. UpdateBatch или.</span><span class="sxs-lookup"><span data-stu-id="40839-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="40839-125">Если вы используете **набор записей**ADO, вы можете использовать его метод [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="40839-126">Использование **UpdateBatch** является рекомендуемым методом для объектов **Recordset** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="40839-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="40839-127">Например, ваш код может быть Мирс. UpdateBatch или ADC1. Recordset. UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="40839-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


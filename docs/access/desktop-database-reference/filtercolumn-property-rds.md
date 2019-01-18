---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711786"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="b4d11-102">Свойство FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="b4d11-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="b4d11-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4d11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4d11-104">Указывает столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4d11-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d11-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4d11-105">Syntax</span></span>

<span data-ttu-id="b4d11-106">*DataControl*. FilterColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="b4d11-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="b4d11-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b4d11-107">Parameters</span></span>

|<span data-ttu-id="b4d11-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b4d11-108">Parameter</span></span>|<span data-ttu-id="b4d11-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b4d11-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b4d11-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b4d11-110">*DataControl*</span></span> |<span data-ttu-id="b4d11-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="b4d11-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="b4d11-112">*String*</span><span class="sxs-lookup"><span data-stu-id="b4d11-112">*String*</span></span> |<span data-ttu-id="b4d11-113">**Строковое** значение, указывающее, столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4d11-113">A **String** value that specifies the column on which to evaluate the filter criteria.</span></span> <span data-ttu-id="b4d11-114">Условия фильтра указанных в свойстве [FilterCriterion](filtercriterion-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="b4d11-114">The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b4d11-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4d11-115">Remarks</span></span>

<span data-ttu-id="b4d11-116">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="b4d11-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="b4d11-117">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="b4d11-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="b4d11-118">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="b4d11-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="b4d11-119">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="b4d11-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


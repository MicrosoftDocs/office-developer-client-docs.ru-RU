---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1af06abc634d0ef1984d325722aac814214b28d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949463"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="79cbf-102">Свойство FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="79cbf-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="79cbf-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79cbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79cbf-104">Указывает столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="79cbf-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="79cbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79cbf-105">Syntax</span></span>

<span data-ttu-id="79cbf-106">*DataControl*. FilterColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="79cbf-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="79cbf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79cbf-107">Parameters</span></span>

|<span data-ttu-id="79cbf-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="79cbf-108">Parameter</span></span>|<span data-ttu-id="79cbf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="79cbf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="79cbf-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="79cbf-110">*DataControl*</span></span> |<span data-ttu-id="79cbf-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="79cbf-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="79cbf-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="79cbf-112">*String*</span></span> |<span data-ttu-id="79cbf-113">**Строковое** значение, указывающее, столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="79cbf-113">A **String** value that specifies the column on which to evaluate the filter criteria.</span></span> <span data-ttu-id="79cbf-114">Условия фильтра указанных в свойстве [FilterCriterion](filtercriterion-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="79cbf-114">The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="79cbf-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="79cbf-115">Remarks</span></span>

<span data-ttu-id="79cbf-116">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="79cbf-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="79cbf-117">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="79cbf-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="79cbf-118">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="79cbf-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="79cbf-119">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="79cbf-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


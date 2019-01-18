---
title: Свойство FilterValue (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721950"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="d7db4-102">Свойство FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="d7db4-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="d7db4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7db4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7db4-104">Указывает значение для фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="d7db4-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7db4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7db4-105">Syntax</span></span>

<span data-ttu-id="d7db4-106">*DataControl*. Значение_фильтра = *строка*</span><span class="sxs-lookup"><span data-stu-id="d7db4-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="d7db4-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d7db4-107">Parameters</span></span>

|<span data-ttu-id="d7db4-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d7db4-108">Parameter</span></span>|<span data-ttu-id="d7db4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d7db4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d7db4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d7db4-110">*DataControl*</span></span> |<span data-ttu-id="d7db4-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="d7db4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="d7db4-112">*String*</span><span class="sxs-lookup"><span data-stu-id="d7db4-112">*String*</span></span> |<span data-ttu-id="d7db4-113">**Строковое** значение, представляющее значение данных для фильтрации записей (например, «Программиста» или 125).</span><span class="sxs-lookup"><span data-stu-id="d7db4-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="d7db4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7db4-114">Remarks</span></span>

<span data-ttu-id="d7db4-115">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **Значение_фильтра**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="d7db4-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="d7db4-116">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="d7db4-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="d7db4-117">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="d7db4-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="d7db4-118">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="d7db4-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="d7db4-119">Ошибка type mismatch привести значения NULL.</span><span class="sxs-lookup"><span data-stu-id="d7db4-119">Null values result in a type mismatch error.</span></span>


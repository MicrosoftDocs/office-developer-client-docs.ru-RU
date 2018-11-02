---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3c9f20b26ff184bcd3f1a24f7f1523acdc5f184
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927391"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="3d0d9-102">Свойство FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="3d0d9-102">FilterColumn property (RDS)</span></span>


<span data-ttu-id="3d0d9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d0d9-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="3d0d9-104">Указывает столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d0d9-105">Syntax</span></span>

<span data-ttu-id="3d0d9-106">*DataControl*. FilterColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="3d0d9-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3d0d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d0d9-107">Parameters</span></span>

  - <span data-ttu-id="3d0d9-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3d0d9-108">*DataControl*</span></span>

  - <span data-ttu-id="3d0d9-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="3d0d9-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="3d0d9-110">*String*</span></span>

  - <span data-ttu-id="3d0d9-111">**Строковое** значение, указывающее, столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-111">A **String** value that specifies the column on which to evaluate the filter criteria.</span></span> <span data-ttu-id="3d0d9-112">Условия фильтра указанных в свойстве [FilterCriterion](filtercriterion-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="3d0d9-112">The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d0d9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d0d9-113">Remarks</span></span>

<span data-ttu-id="3d0d9-114">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-114">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="3d0d9-115">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-115">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="3d0d9-116">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-116">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="3d0d9-117">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="3d0d9-117">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cf03a2cbff06919981ac940f5b2962062a850c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877802"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="75f99-102">Свойство FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="75f99-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="75f99-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75f99-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="75f99-104">Указывает столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="75f99-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75f99-105">Syntax</span></span>

<span data-ttu-id="75f99-106">*DataControl*. FilterColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="75f99-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="75f99-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75f99-107">Parameters</span></span>

  - <span data-ttu-id="75f99-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="75f99-108">*DataControl*</span></span>

  - <span data-ttu-id="75f99-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="75f99-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="75f99-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="75f99-110">*String*</span></span>

  - <span data-ttu-id="75f99-111">**Строковое** значение, указывающее, столбец, по которому для оценки условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="75f99-111">A **String** value that specifies the column on which to evaluate the filter criteria.</span></span> <span data-ttu-id="75f99-112">Условия фильтра указанных в свойстве [FilterCriterion](filtercriterion-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="75f99-112">The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f99-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="75f99-113">Remarks</span></span>

<span data-ttu-id="75f99-114">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="75f99-114">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="75f99-115">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="75f99-115">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="75f99-116">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="75f99-116">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="75f99-117">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="75f99-117">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


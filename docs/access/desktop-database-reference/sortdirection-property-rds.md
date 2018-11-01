---
title: Свойство направления сортировки (RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3603696992ab7ac759a62a70f50b4fa35636d2c0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879153"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="c0878-102">Свойство направления сортировки (RDS)</span><span class="sxs-lookup"><span data-stu-id="c0878-102">SortDirection Property (RDS)</span></span>


<span data-ttu-id="c0878-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0878-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c0878-104">Указывает, будет ли порядок сортировки по возрастанию или по убыванию.</span><span class="sxs-lookup"><span data-stu-id="c0878-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0878-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0878-105">Syntax</span></span>

<span data-ttu-id="c0878-106">*DataControl*. Направления сортировки = *значение*</span><span class="sxs-lookup"><span data-stu-id="c0878-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="c0878-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0878-107">Parameters</span></span>

  - <span data-ttu-id="c0878-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c0878-108">*DataControl*</span></span>

  - <span data-ttu-id="c0878-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="c0878-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="c0878-110">*Значение*</span><span class="sxs-lookup"><span data-stu-id="c0878-110">*Value*</span></span>

  - <span data-ttu-id="c0878-111">**Логическое** значение, если параметр имеет значение **True**, указывающее направление сортировки по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="c0878-111">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending.</span></span> <span data-ttu-id="c0878-112">**Значение false** указывает убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="c0878-112">**False** indicates descending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0878-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0878-113">Remarks</span></span>

<span data-ttu-id="c0878-114">[SortColumn](sortcolumn-property-rds.md), **SortDirection**, [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="c0878-114">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="c0878-115">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="c0878-115">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="c0878-116">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="c0878-116">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="c0878-117">Метод **Reset** будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="c0878-117">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


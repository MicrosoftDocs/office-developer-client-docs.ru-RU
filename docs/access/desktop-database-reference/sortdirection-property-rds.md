---
title: Свойство SortDirection (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd09eb22d9f751ab1140db948356d2b168b30afb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711359"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="133cd-102">Свойство SortDirection (RDS)</span><span class="sxs-lookup"><span data-stu-id="133cd-102">SortDirection property (RDS)</span></span>

<span data-ttu-id="133cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="133cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="133cd-104">Указывает, будет ли порядок сортировки по возрастанию или по убыванию.</span><span class="sxs-lookup"><span data-stu-id="133cd-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="133cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="133cd-105">Syntax</span></span>

<span data-ttu-id="133cd-106">*DataControl*. Направления сортировки = *значение*</span><span class="sxs-lookup"><span data-stu-id="133cd-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="133cd-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="133cd-107">Parameters</span></span>

|<span data-ttu-id="133cd-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="133cd-108">Parameter</span></span>|<span data-ttu-id="133cd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="133cd-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="133cd-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="133cd-110">*DataControl*</span></span> |<span data-ttu-id="133cd-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="133cd-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="133cd-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="133cd-112">*Value*</span></span> |<span data-ttu-id="133cd-113">**Логическое** значение, если параметр имеет значение **True**, указывающее направление сортировки по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="133cd-113">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending.</span></span> <span data-ttu-id="133cd-114">**Значение false** указывает убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="133cd-114">**False** indicates descending order.</span></span>|

## <a name="remarks"></a><span data-ttu-id="133cd-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="133cd-115">Remarks</span></span>

<span data-ttu-id="133cd-116">[SortColumn](sortcolumn-property-rds.md), **SortDirection**, [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="133cd-116">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="133cd-117">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="133cd-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="133cd-118">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="133cd-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="133cd-119">Метод **Reset** будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="133cd-119">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308619"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="452ac-102">Свойство SortDirection (RDS)</span><span class="sxs-lookup"><span data-stu-id="452ac-102">SortDirection property (RDS)</span></span>

<span data-ttu-id="452ac-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="452ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="452ac-104">Указывает, является ли порядок сортировки восходящим или нисходящим.</span><span class="sxs-lookup"><span data-stu-id="452ac-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="452ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="452ac-105">Syntax</span></span>

<span data-ttu-id="452ac-106">*DataControl*. SortDirection = *значение*</span><span class="sxs-lookup"><span data-stu-id="452ac-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="452ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="452ac-107">Parameters</span></span>

|<span data-ttu-id="452ac-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="452ac-108">Parameter</span></span>|<span data-ttu-id="452ac-109">Описание</span><span class="sxs-lookup"><span data-stu-id="452ac-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="452ac-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="452ac-110">*DataControl*</span></span> |<span data-ttu-id="452ac-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="452ac-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="452ac-112">*Значение*</span><span class="sxs-lookup"><span data-stu-id="452ac-112">*Value*</span></span> |<span data-ttu-id="452ac-113">Значение **Boolean,** которое при заданном **значении True** указывает на восходящее направление сортировки.</span><span class="sxs-lookup"><span data-stu-id="452ac-113">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending.</span></span> <span data-ttu-id="452ac-114">**False** указывает порядок убывания.</span><span class="sxs-lookup"><span data-stu-id="452ac-114">**False** indicates descending order.</span></span>|

## <a name="remarks"></a><span data-ttu-id="452ac-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="452ac-115">Remarks</span></span>

<span data-ttu-id="452ac-116">Свойства [SortColumn,](sortcolumn-property-rds.md) **SortDirection,** [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="452ac-116">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="452ac-117">Функция сортировки заказывает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="452ac-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="452ac-118">Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше.</span><span class="sxs-lookup"><span data-stu-id="452ac-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="452ac-119">Метод **Reset** выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="452ac-119">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


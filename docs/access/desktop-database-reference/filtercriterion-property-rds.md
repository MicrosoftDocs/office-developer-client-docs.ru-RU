---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292428"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="226b5-102">Свойство FilterCriterion (RDS)</span><span class="sxs-lookup"><span data-stu-id="226b5-102">FilterCriterion property (RDS)</span></span>

<span data-ttu-id="226b5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="226b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="226b5-104">Указывает оператор оценки для использования в значении фильтра.</span><span class="sxs-lookup"><span data-stu-id="226b5-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="226b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="226b5-105">Syntax</span></span>

<span data-ttu-id="226b5-106">*DataControl*. FilterCriterion = *String*</span><span class="sxs-lookup"><span data-stu-id="226b5-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="226b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="226b5-107">Parameters</span></span>

|<span data-ttu-id="226b5-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="226b5-108">Parameter</span></span>|<span data-ttu-id="226b5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="226b5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="226b5-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="226b5-110">*DataControl*</span></span> |<span data-ttu-id="226b5-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="226b5-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="226b5-112">*String*</span><span class="sxs-lookup"><span data-stu-id="226b5-112">*String*</span></span> |<span data-ttu-id="226b5-113">Значение **String,** которое указывает оператор оценки [FilterValue](filtervalue-property-rds.md) для записей.</span><span class="sxs-lookup"><span data-stu-id="226b5-113">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="226b5-114">Может быть любой из следующих: \< \< =, \> \> =, =, =, или \< \> .</span><span class="sxs-lookup"><span data-stu-id="226b5-114">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>|

## <a name="remarks"></a><span data-ttu-id="226b5-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="226b5-115">Remarks</span></span>

<span data-ttu-id="226b5-116">Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) **FilterCriterion** и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="226b5-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="226b5-117">Функция сортировки заказывает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="226b5-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="226b5-118">Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше.</span><span class="sxs-lookup"><span data-stu-id="226b5-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="226b5-119">Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="226b5-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="226b5-120">Оператор \! "=" не действителен для **FilterCriterion;** вместо этого используйте \< \> ".</span><span class="sxs-lookup"><span data-stu-id="226b5-120">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="226b5-121">Если установлены свойства фильтра и сортировки, и вы называете метод **Reset,** сначала фильтруется набор строк, а затем сортироваться.</span><span class="sxs-lookup"><span data-stu-id="226b5-121">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted.</span></span> <span data-ttu-id="226b5-122">Для восходящих сортов значения null находятся в верхней части; для убывающих сортов значения null находятся в нижней части (восходящий — это поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="226b5-122">For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292407"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="dbbe4-102">Свойство FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="dbbe4-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="dbbe4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbbe4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbbe4-104">Указывает значение для фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbbe4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbbe4-105">Syntax</span></span>

<span data-ttu-id="dbbe4-106">*DataControl*. FilterValue = *String*</span><span class="sxs-lookup"><span data-stu-id="dbbe4-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="dbbe4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbbe4-107">Parameters</span></span>

|<span data-ttu-id="dbbe4-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="dbbe4-108">Parameter</span></span>|<span data-ttu-id="dbbe4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dbbe4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dbbe4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="dbbe4-110">*DataControl*</span></span> |<span data-ttu-id="dbbe4-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="dbbe4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="dbbe4-112">*String*</span><span class="sxs-lookup"><span data-stu-id="dbbe4-112">*String*</span></span> |<span data-ttu-id="dbbe4-113">Значение **String,** представляю которое представляет значение данных для фильтрации записей (например, "Программист" или 125).</span><span class="sxs-lookup"><span data-stu-id="dbbe4-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="dbbe4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbbe4-114">Remarks</span></span>

<span data-ttu-id="dbbe4-115">Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) **FilterValue,** [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="dbbe4-116">Функция сортировки заказывает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="dbbe4-117">Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="dbbe4-118">Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="dbbe4-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="dbbe4-119">Значения Null приводит к ошибке несоответствия типа.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-119">Null values result in a type mismatch error.</span></span>


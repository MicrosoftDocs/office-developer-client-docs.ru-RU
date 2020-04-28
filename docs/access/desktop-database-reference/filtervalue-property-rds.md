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
# <a name="filtervalue-property-rds"></a><span data-ttu-id="6cc86-102">Свойство FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="6cc86-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="6cc86-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cc86-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cc86-104">Указывает значение, с которым отфильтровать записи.</span><span class="sxs-lookup"><span data-stu-id="6cc86-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cc86-105">Syntax</span></span>

<span data-ttu-id="6cc86-106">*Элемент управления*. FilterValue = *строка*</span><span class="sxs-lookup"><span data-stu-id="6cc86-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc86-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cc86-107">Parameters</span></span>

|<span data-ttu-id="6cc86-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="6cc86-108">Parameter</span></span>|<span data-ttu-id="6cc86-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc86-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6cc86-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="6cc86-110">*DataControl*</span></span> |<span data-ttu-id="6cc86-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="6cc86-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="6cc86-112">*String*</span><span class="sxs-lookup"><span data-stu-id="6cc86-112">*String*</span></span> |<span data-ttu-id="6cc86-113">**Строковое** значение, представляющее значение данных, с которым отфильтруются записи (например, "программист" или "125").</span><span class="sxs-lookup"><span data-stu-id="6cc86-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="6cc86-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6cc86-114">Remarks</span></span>

<span data-ttu-id="6cc86-115">Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="6cc86-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="6cc86-116">Функция сортировки упорядочивает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="6cc86-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="6cc86-117">Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc86-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="6cc86-118">Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** **записей на обновляемый.**</span><span class="sxs-lookup"><span data-stu-id="6cc86-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="6cc86-119">Значения NULL приводят к ошибке несоответствия типа.</span><span class="sxs-lookup"><span data-stu-id="6cc86-119">Null values result in a type mismatch error.</span></span>


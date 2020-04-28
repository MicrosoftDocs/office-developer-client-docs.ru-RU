---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292442"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="c6272-102">Свойство FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="c6272-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="c6272-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6272-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6272-104">Указывает столбец, для которого необходимо оценить условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="c6272-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6272-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6272-105">Syntax</span></span>

<span data-ttu-id="c6272-106">*Элемент управления*. FilterColumn = *строка*</span><span class="sxs-lookup"><span data-stu-id="c6272-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="c6272-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6272-107">Parameters</span></span>

|<span data-ttu-id="c6272-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c6272-108">Parameter</span></span>|<span data-ttu-id="c6272-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c6272-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c6272-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c6272-110">*DataControl*</span></span> |<span data-ttu-id="c6272-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="c6272-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="c6272-112">*String*</span><span class="sxs-lookup"><span data-stu-id="c6272-112">*String*</span></span> |<span data-ttu-id="c6272-113">**Строковое** значение, задающее столбец, для которого необходимо оценить условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="c6272-113">A **String** value that specifies the column on which to evaluate the filter criteria.</span></span> <span data-ttu-id="c6272-114">Условия фильтра указываются в свойстве [FilterCriterion](filtercriterion-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="c6272-114">The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c6272-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6272-115">Remarks</span></span>

<span data-ttu-id="c6272-116">Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** предоставляют функции сортировки и фильтрации кэша на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="c6272-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="c6272-117">Функция сортировки упорядочивает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="c6272-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="c6272-118">Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c6272-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="c6272-119">Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** **записей на обновляемый.**</span><span class="sxs-lookup"><span data-stu-id="c6272-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>


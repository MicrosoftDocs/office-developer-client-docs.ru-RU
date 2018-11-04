---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9887551d4d8a141c8390764bcd23c98c59edc26
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950225"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="7563f-102">Свойство FilterCriterion (RDS)</span><span class="sxs-lookup"><span data-stu-id="7563f-102">FilterCriterion property (RDS)</span></span>

<span data-ttu-id="7563f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7563f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7563f-104">Указывает оператор оценки, используемый в значение фильтра.</span><span class="sxs-lookup"><span data-stu-id="7563f-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7563f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7563f-105">Syntax</span></span>

<span data-ttu-id="7563f-106">*DataControl*. FilterCriterion = *строка*</span><span class="sxs-lookup"><span data-stu-id="7563f-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="7563f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7563f-107">Parameters</span></span>

|<span data-ttu-id="7563f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="7563f-108">Parameter</span></span>|<span data-ttu-id="7563f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7563f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7563f-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="7563f-110">*DataControl*</span></span> |<span data-ttu-id="7563f-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="7563f-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="7563f-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="7563f-112">*String*</span></span> |<span data-ttu-id="7563f-113">**Строковое** значение, указывающее, оператор оценки [Значение_фильтра](filtervalue-property-rds.md) в записи.</span><span class="sxs-lookup"><span data-stu-id="7563f-113">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="7563f-114">Может быть одним из следующих значений: \<, \<=, \>, \>=, =, или \< \>.</span><span class="sxs-lookup"><span data-stu-id="7563f-114">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7563f-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7563f-115">Remarks</span></span>

<span data-ttu-id="7563f-116">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), **FilterCriterion**и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="7563f-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="7563f-117">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="7563f-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="7563f-118">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="7563f-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="7563f-119">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="7563f-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="7563f-120">"\!=» Недопустимый оператор для **FilterCriterion**; Используйте "\<\>«.</span><span class="sxs-lookup"><span data-stu-id="7563f-120">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="7563f-121">Если задать свойства фильтрации и сортировки, вызовите метод **Сброс** набор строк сначала фильтруется и затем сортировки.</span><span class="sxs-lookup"><span data-stu-id="7563f-121">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted.</span></span> <span data-ttu-id="7563f-122">Для сортировки в порядке возрастания, пустые значения отображаются сверху; для Сортировка по убыванию значения null, в нижней (по возрастанию — это поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7563f-122">For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>


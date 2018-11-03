---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a9724d84bed6c89267aeb811936eeb49b49bc17
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929344"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="52851-102">Свойство FilterCriterion (RDS)</span><span class="sxs-lookup"><span data-stu-id="52851-102">FilterCriterion property (RDS)</span></span>


<span data-ttu-id="52851-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52851-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="52851-104">Указывает оператор оценки, используемый в значение фильтра.</span><span class="sxs-lookup"><span data-stu-id="52851-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="52851-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52851-105">Syntax</span></span>

<span data-ttu-id="52851-106">*DataControl*. FilterCriterion = *строка*</span><span class="sxs-lookup"><span data-stu-id="52851-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="52851-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="52851-107">Parameters</span></span>

  - <span data-ttu-id="52851-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="52851-108">*DataControl*</span></span>

  - <span data-ttu-id="52851-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="52851-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="52851-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="52851-110">*String*</span></span>

  - <span data-ttu-id="52851-111">**Строковое** значение, указывающее, оператор оценки [Значение_фильтра](filtervalue-property-rds.md) в записи.</span><span class="sxs-lookup"><span data-stu-id="52851-111">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="52851-112">Может быть одним из следующих значений: \<, \<=, \>, \>=, =, или \< \>.</span><span class="sxs-lookup"><span data-stu-id="52851-112">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>

## <a name="remarks"></a><span data-ttu-id="52851-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="52851-113">Remarks</span></span>

<span data-ttu-id="52851-114">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), **FilterCriterion**и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="52851-114">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="52851-115">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="52851-115">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="52851-116">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="52851-116">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="52851-117">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="52851-117">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="52851-118">"\!=» Недопустимый оператор для **FilterCriterion**; Используйте "\<\>«.</span><span class="sxs-lookup"><span data-stu-id="52851-118">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="52851-119">Если задать свойства фильтрации и сортировки, вызовите метод **Сброс** набор строк сначала фильтруется и затем сортировки.</span><span class="sxs-lookup"><span data-stu-id="52851-119">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted.</span></span> <span data-ttu-id="52851-120">Для сортировки в порядке возрастания, пустые значения отображаются сверху; для Сортировка по убыванию значения null, в нижней (по возрастанию — это поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="52851-120">For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>


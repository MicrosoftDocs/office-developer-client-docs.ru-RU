---
title: Метод Reset (RDS - ссылки для настольных баз данных Access)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714242"
---
# <a name="reset-method-rds"></a><span data-ttu-id="2d864-102">Метод Reset (RDS)</span><span class="sxs-lookup"><span data-stu-id="2d864-102">Reset method (RDS)</span></span>

<span data-ttu-id="2d864-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d864-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d864-104">Выполняет сортировки или фильтрации со стороны клиента **набора записей** на основе указанного программная сортировка и фильтр свойств.</span><span class="sxs-lookup"><span data-stu-id="2d864-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d864-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d864-105">Syntax</span></span>

<span data-ttu-id="2d864-106">*DataControl*. Reset (*значение*)</span><span class="sxs-lookup"><span data-stu-id="2d864-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2d864-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d864-107">Parameters</span></span>

|<span data-ttu-id="2d864-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2d864-108">Parameter</span></span>|<span data-ttu-id="2d864-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2d864-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2d864-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2d864-110">*DataControl*</span></span> |<span data-ttu-id="2d864-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="2d864-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="2d864-112">*value*</span><span class="sxs-lookup"><span data-stu-id="2d864-112">*value*</span></span> |<span data-ttu-id="2d864-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2d864-113">Optional.</span></span> <span data-ttu-id="2d864-114">**Логическое** значение, равное **True** (по умолчанию) Если требуется отфильтровать на текущем «отфильтрованные» строк.</span><span class="sxs-lookup"><span data-stu-id="2d864-114">A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset.</span></span> <span data-ttu-id="2d864-115">**Значение false** указывает, что фильтрации на исходной строк, удалить любые предыдущие параметры фильтра.</span><span class="sxs-lookup"><span data-stu-id="2d864-115">**False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2d864-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d864-116">Remarks</span></span>

<span data-ttu-id="2d864-117">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="2d864-117">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="2d864-118">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="2d864-118">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="2d864-119">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="2d864-119">The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="2d864-120">Метод **Reset** будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="2d864-120">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="2d864-121">При внесении изменений в исходных данных, который еще не был отправлен, метод **Сброс** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2d864-121">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail.</span></span> <span data-ttu-id="2d864-122">Во-первых используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в чтение и запись **набора записей**, а затем **сбросить** метод для сортировки или фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="2d864-122">First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="2d864-123">Если вы хотите выполнить более одного фильтра на набора строк, можно использовать необязательный аргумент *Boolean* с помощью метода **сбросить** .</span><span class="sxs-lookup"><span data-stu-id="2d864-123">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="2d864-124">Следующем примере показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="2d864-124">The following example shows how to do this:</span></span>


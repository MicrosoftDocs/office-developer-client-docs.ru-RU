---
title: Метод Reset (Справочник по базам данных для рабочих столов службы RDS)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306645"
---
# <a name="reset-method-rds"></a><span data-ttu-id="79255-102">Метод Reset (RDS)</span><span class="sxs-lookup"><span data-stu-id="79255-102">Reset method (RDS)</span></span>

<span data-ttu-id="79255-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79255-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79255-104">Выполняет сортировку или фильтрацию на клиентском объекте **Recordset** на основе указанных свойств сортировки и фильтра.</span><span class="sxs-lookup"><span data-stu-id="79255-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79255-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79255-105">Syntax</span></span>

<span data-ttu-id="79255-106">*Элемент управления*. Сброс (*значение*)</span><span class="sxs-lookup"><span data-stu-id="79255-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="79255-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79255-107">Parameters</span></span>

|<span data-ttu-id="79255-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="79255-108">Parameter</span></span>|<span data-ttu-id="79255-109">Описание</span><span class="sxs-lookup"><span data-stu-id="79255-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="79255-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="79255-110">*DataControl*</span></span> |<span data-ttu-id="79255-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="79255-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="79255-112">*value*</span><span class="sxs-lookup"><span data-stu-id="79255-112">*value*</span></span> |<span data-ttu-id="79255-113">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="79255-113">Optional.</span></span> <span data-ttu-id="79255-114">**Логическое** значение **true** (по умолчанию), если требуется фильтровать по текущему набору строк "filtered".</span><span class="sxs-lookup"><span data-stu-id="79255-114">A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset.</span></span> <span data-ttu-id="79255-115">**Значение false** означает, что выполняется фильтрация по исходному набору строк с удалением всех предыдущих параметров фильтра.</span><span class="sxs-lookup"><span data-stu-id="79255-115">**False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="79255-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="79255-116">Remarks</span></span>

<span data-ttu-id="79255-117">Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="79255-117">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="79255-118">Функция сортировки упорядочивает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="79255-118">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="79255-119">Функция фильтрации отображает подмножество записей на основе условий поиска, а полный [набор записей](recordset-object-ado.md) сохраняется в кэше.</span><span class="sxs-lookup"><span data-stu-id="79255-119">The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="79255-120">Метод **Reset** выполнит условия и заменит текущий **набор** **записей на обновляемый.**</span><span class="sxs-lookup"><span data-stu-id="79255-120">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="79255-121">При изменении исходных данных, которые еще не были отправлены, метод **Reset** завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="79255-121">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail.</span></span> <span data-ttu-id="79255-122">Сначала используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в **наборе записей**для чтения и записи, а затем используйте метод **Reset** для сортировки или фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="79255-122">First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="79255-123">Если вы хотите выполнить несколько фильтров для набора строк, вы можете использовать необязательный *логический* аргумент с методом **Reset** .</span><span class="sxs-lookup"><span data-stu-id="79255-123">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="79255-124">В приведенном ниже примере показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="79255-124">The following example shows how to do this:</span></span>


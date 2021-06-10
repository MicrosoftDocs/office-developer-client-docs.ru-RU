---
title: Метод сброса (RDS - ссылка на настольные базы данных)
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
# <a name="reset-method-rds"></a><span data-ttu-id="2ab6b-102">Метод сброса (RDS)</span><span class="sxs-lookup"><span data-stu-id="2ab6b-102">Reset method (RDS)</span></span>

<span data-ttu-id="2ab6b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ab6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ab6b-104">Выполняет сортировку или фильтрацию на клиентском наборе **recordset** на основе указанных свойств сортировки и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ab6b-105">Syntax</span></span>

<span data-ttu-id="2ab6b-106">*DataControl*. Сброс *(значение*)</span><span class="sxs-lookup"><span data-stu-id="2ab6b-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2ab6b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ab6b-107">Parameters</span></span>

|<span data-ttu-id="2ab6b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2ab6b-108">Parameter</span></span>|<span data-ttu-id="2ab6b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2ab6b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2ab6b-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2ab6b-110">*DataControl*</span></span> |<span data-ttu-id="2ab6b-111">Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="2ab6b-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="2ab6b-112">*value*</span><span class="sxs-lookup"><span data-stu-id="2ab6b-112">*value*</span></span> |<span data-ttu-id="2ab6b-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-113">Optional.</span></span> <span data-ttu-id="2ab6b-114">Значение **Boolean** true **(по** умолчанию), если необходимо фильтровать текущий "фильтрованный" набор строк.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-114">A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset.</span></span> <span data-ttu-id="2ab6b-115">**False** указывает, что вы фильтруете исходный набор строк, удаляя все предыдущие параметры фильтра.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-115">**False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2ab6b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ab6b-116">Remarks</span></span>

<span data-ttu-id="2ab6b-117">Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-117">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="2ab6b-118">Функция сортировки заказывает записи по значениям из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-118">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="2ab6b-119">Функция фильтрации отображает подмножество записей на основе критериев поиска, а полный набор [записей](recordset-object-ado.md) поддерживается в кэше.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-119">The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="2ab6b-120">Метод **Reset** выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-120">The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="2ab6b-121">Если будут внесены изменения в исходные данные, которые еще не были отправлены, метод **Сброса** не удастся.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-121">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail.</span></span> <span data-ttu-id="2ab6b-122">Сначала используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в наборе записей чтения и записи, а затем используйте метод **Reset** для сортировки или фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-122">First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="2ab6b-123">Если вы хотите выполнить несколько фильтров в строковом наборе, можно использовать необязательный аргумент *Boolean* с помощью метода **Reset.**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-123">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="2ab6b-124">В следующем примере показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="2ab6b-124">The following example shows how to do this:</span></span>


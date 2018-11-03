---
title: Свойство FilterValue (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2573500fe47c69dfd1779ecc4ad5e0abb7dcf8c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925305"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="34546-102">Свойство FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="34546-102">FilterValue property (RDS)</span></span>


<span data-ttu-id="34546-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34546-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="34546-104">Указывает значение для фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="34546-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="34546-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34546-105">Syntax</span></span>

<span data-ttu-id="34546-106">*DataControl*. Значение_фильтра = *строка*</span><span class="sxs-lookup"><span data-stu-id="34546-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="34546-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34546-107">Parameters</span></span>

  - <span data-ttu-id="34546-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="34546-108">*DataControl*</span></span>

  - <span data-ttu-id="34546-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="34546-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="34546-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="34546-110">*String*</span></span>

  - <span data-ttu-id="34546-111">**Строковое** значение, представляющее значение данных для фильтрации записей (например, «Программиста» или 125).</span><span class="sxs-lookup"><span data-stu-id="34546-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="34546-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="34546-112">Remarks</span></span>

<span data-ttu-id="34546-113">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **Значение_фильтра**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="34546-113">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="34546-114">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="34546-114">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="34546-115">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="34546-115">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="34546-116">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="34546-116">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="34546-117">Ошибка type mismatch привести значения NULL.</span><span class="sxs-lookup"><span data-stu-id="34546-117">Null values result in a type mismatch error.</span></span>


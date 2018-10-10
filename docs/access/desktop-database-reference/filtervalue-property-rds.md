---
title: FilterValue Property (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39152be2c53dc0de9bc1bcb21fee505fcb9106dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480942"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="096d1-102">FilterValue Property (RDS)</span><span class="sxs-lookup"><span data-stu-id="096d1-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="096d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="096d1-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="096d1-104">Указывает значение для фильтрации записей.</span><span class="sxs-lookup"><span data-stu-id="096d1-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="096d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="096d1-105">Syntax</span></span>

<span data-ttu-id="096d1-106">*DataControl*. Значение_фильтра = *строка*</span><span class="sxs-lookup"><span data-stu-id="096d1-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="096d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="096d1-107">Parameters</span></span>

  - <span data-ttu-id="096d1-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="096d1-108">*DataControl*</span></span>

  - <span data-ttu-id="096d1-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="096d1-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="096d1-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="096d1-110">*String*</span></span>

  - <span data-ttu-id="096d1-111">**Строковое** значение, представляющее значение данных для фильтрации записей (например, «Программиста» или 125).</span><span class="sxs-lookup"><span data-stu-id="096d1-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="096d1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="096d1-112">Remarks</span></span>

<span data-ttu-id="096d1-113">[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **Значение_фильтра**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="096d1-113">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> <span data-ttu-id="096d1-114">Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца.</span><span class="sxs-lookup"><span data-stu-id="096d1-114">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="096d1-115">Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше.</span><span class="sxs-lookup"><span data-stu-id="096d1-115">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="096d1-116">Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="096d1-116">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="096d1-117">Ошибка type mismatch привести значения NULL.</span><span class="sxs-lookup"><span data-stu-id="096d1-117">Null values result in a type mismatch error.</span></span>


---
title: Метод CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712164"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="30e17-102">Метод CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="30e17-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="30e17-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30e17-104">Сравнение двух закладки и возвращает сведения об их значения.</span><span class="sxs-lookup"><span data-stu-id="30e17-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30e17-105">Syntax</span></span>

<span data-ttu-id="30e17-106">*результат* = *набора записей*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="30e17-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="30e17-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30e17-107">Return value</span></span>

<span data-ttu-id="30e17-108">Возвращает [CompareEnum](compareenum.md) значение, указывающее положение относительно строки из двух записей, представленное закладок.</span><span class="sxs-lookup"><span data-stu-id="30e17-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="30e17-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="30e17-109">Parameters</span></span>

|<span data-ttu-id="30e17-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="30e17-110">Parameter</span></span>|<span data-ttu-id="30e17-111">Описание</span><span class="sxs-lookup"><span data-stu-id="30e17-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="30e17-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="30e17-112">*Bookmark1*</span></span> |<span data-ttu-id="30e17-113">Закладка первой строки.</span><span class="sxs-lookup"><span data-stu-id="30e17-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="30e17-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="30e17-114">*Bookmark2*</span></span> |<span data-ttu-id="30e17-115">Закладка второй строке.</span><span class="sxs-lookup"><span data-stu-id="30e17-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="30e17-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="30e17-116">Remarks</span></span>

<span data-ttu-id="30e17-117">Закладки необходимо установить на тот же объект [набора записей](recordset-object-ado.md) или объекта **набора записей** и его [копия](clone-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="30e17-117">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md).</span></span> <span data-ttu-id="30e17-118">Сравнение надежно закладок из разных объектов **набора записей** , даже в том случае, если они были созданы на основе команду или источника.</span><span class="sxs-lookup"><span data-stu-id="30e17-118">You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command.</span></span> <span data-ttu-id="30e17-119">Ни сравнение закладки для объекта **набора записей** , основной поставщик не поддерживает сравнения.</span><span class="sxs-lookup"><span data-stu-id="30e17-119">Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="30e17-120">Закладка уникально идентифицирует строки в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="30e17-120">A bookmark uniquely identifies a row in a **Recordset** object.</span></span> <span data-ttu-id="30e17-121">Свойство [закладку](bookmark-property-ado.md) текущей строки используется для получения ее закладки.</span><span class="sxs-lookup"><span data-stu-id="30e17-121">Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="30e17-122">Так как тип данных закладки зависит от поставщика, ADO представляет его как переменную типа Variant.</span><span class="sxs-lookup"><span data-stu-id="30e17-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="30e17-123">К примеру, закладки SQL Server имеют тип DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="30e17-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="30e17-124">ADO предоставить этот тип в качестве типа Variant с подтипом типа Double.</span><span class="sxs-lookup"><span data-stu-id="30e17-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="30e17-125">При сравнении закладки, ADO не пытается любого типа приведения.</span><span class="sxs-lookup"><span data-stu-id="30e17-125">When comparing bookmarks, ADO does not attempt any type of coercion.</span></span> <span data-ttu-id="30e17-126">Значения, просто передаются в поставщик где происходит сравнить.</span><span class="sxs-lookup"><span data-stu-id="30e17-126">The values are simply passed to the provider where the compare occurs.</span></span> <span data-ttu-id="30e17-127">Если закладки, переданной в метод **CompareBookmarks** хранятся в переменных различных типов, его можно создать ошибка type mismatch «Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.»</span><span class="sxs-lookup"><span data-stu-id="30e17-127">If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="30e17-128">Закладки, который не является допустимым или неправильно сформированные приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="30e17-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


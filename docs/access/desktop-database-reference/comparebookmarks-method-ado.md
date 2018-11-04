---
title: Метод CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8b4ff47c0fa778e89479df7a4281abd534fdcec8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949626"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="34e2a-102">Метод CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="34e2a-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="34e2a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34e2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34e2a-104">Сравнение двух закладки и возвращает сведения об их значения.</span><span class="sxs-lookup"><span data-stu-id="34e2a-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34e2a-105">Syntax</span></span>

<span data-ttu-id="34e2a-106">*результат* = *набора записей*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="34e2a-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="34e2a-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34e2a-107">Return value</span></span>

<span data-ttu-id="34e2a-108">Возвращает [CompareEnum](compareenum.md) значение, указывающее положение относительно строки из двух записей, представленное закладок.</span><span class="sxs-lookup"><span data-stu-id="34e2a-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="34e2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="34e2a-109">Parameters</span></span>

|<span data-ttu-id="34e2a-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="34e2a-110">Parameter</span></span>|<span data-ttu-id="34e2a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="34e2a-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="34e2a-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="34e2a-112">*Bookmark1*</span></span> |<span data-ttu-id="34e2a-113">Закладка первой строки.</span><span class="sxs-lookup"><span data-stu-id="34e2a-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="34e2a-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="34e2a-114">*Bookmark2*</span></span> |<span data-ttu-id="34e2a-115">Закладка второй строке.</span><span class="sxs-lookup"><span data-stu-id="34e2a-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="34e2a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="34e2a-116">Remarks</span></span>

<span data-ttu-id="34e2a-117">Закладки необходимо установить на тот же объект [набора записей](recordset-object-ado.md) или объекта **набора записей** и его [копия](clone-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="34e2a-117">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md).</span></span> <span data-ttu-id="34e2a-118">Сравнение надежно закладок из разных объектов **набора записей** , даже в том случае, если они были созданы на основе команду или источника.</span><span class="sxs-lookup"><span data-stu-id="34e2a-118">You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command.</span></span> <span data-ttu-id="34e2a-119">Ни сравнение закладки для объекта **набора записей** , основной поставщик не поддерживает сравнения.</span><span class="sxs-lookup"><span data-stu-id="34e2a-119">Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="34e2a-120">Закладка уникально идентифицирует строки в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="34e2a-120">A bookmark uniquely identifies a row in a **Recordset** object.</span></span> <span data-ttu-id="34e2a-121">Свойство [закладку](bookmark-property-ado.md) текущей строки используется для получения ее закладки.</span><span class="sxs-lookup"><span data-stu-id="34e2a-121">Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="34e2a-122">Так как тип данных закладки зависит от поставщика, ADO представляет его как переменную типа Variant.</span><span class="sxs-lookup"><span data-stu-id="34e2a-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="34e2a-123">К примеру, закладки SQL Server имеют тип DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="34e2a-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="34e2a-124">ADO предоставить этот тип в качестве типа Variant с подтипом типа Double.</span><span class="sxs-lookup"><span data-stu-id="34e2a-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="34e2a-125">При сравнении закладки, ADO не пытается любого типа приведения.</span><span class="sxs-lookup"><span data-stu-id="34e2a-125">When comparing bookmarks, ADO does not attempt any type of coercion.</span></span> <span data-ttu-id="34e2a-126">Значения, просто передаются в поставщик где происходит сравнить.</span><span class="sxs-lookup"><span data-stu-id="34e2a-126">The values are simply passed to the provider where the compare occurs.</span></span> <span data-ttu-id="34e2a-127">Если закладки, переданной в метод **CompareBookmarks** хранятся в переменных различных типов, его можно создать ошибка type mismatch «Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.»</span><span class="sxs-lookup"><span data-stu-id="34e2a-127">If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="34e2a-128">Закладки, который не является допустимым или неправильно сформированные приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="34e2a-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


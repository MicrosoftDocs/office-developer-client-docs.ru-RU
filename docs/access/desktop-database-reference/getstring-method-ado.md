---
title: Метод GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4926b3568d6c7289ca9d3158a8723e016ed344
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949675"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="19041-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="19041-102">GetString method (ADO)</span></span>

<span data-ttu-id="19041-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19041-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19041-104">Возвращает [набор записей](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="19041-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="19041-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19041-105">Syntax</span></span>

<span data-ttu-id="19041-106">*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="19041-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="19041-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19041-107">Return value</span></span>

<span data-ttu-id="19041-108">Возвращает **набор записей** как строковое значение **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="19041-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="19041-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="19041-109">Parameters</span></span>

|<span data-ttu-id="19041-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="19041-110">Parameter</span></span>|<span data-ttu-id="19041-111">Описание</span><span class="sxs-lookup"><span data-stu-id="19041-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="19041-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="19041-112">*StringFormat*</span></span> |<span data-ttu-id="19041-113">[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string.</span><span class="sxs-lookup"><span data-stu-id="19041-113">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="19041-114">Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="19041-114">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="19041-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="19041-115">*NumRows*</span></span> |<span data-ttu-id="19041-116">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="19041-116">Optional.</span></span> <span data-ttu-id="19041-117">Количество строк, преобразуется в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="19041-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="19041-118">Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="19041-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="19041-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="19041-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="19041-120">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="19041-120">Optional.</span></span> <span data-ttu-id="19041-121">Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="19041-121">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="19041-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="19041-122">*RowDelimiter*</span></span> |<span data-ttu-id="19041-123">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="19041-123">Optional.</span></span> <span data-ttu-id="19041-124">Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="19041-124">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="19041-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="19041-125">*NullExpr*</span></span> |<span data-ttu-id="19041-126">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="19041-126">Optional.</span></span> <span data-ttu-id="19041-127">Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="19041-127">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="19041-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="19041-128">Remarks</span></span>

<span data-ttu-id="19041-129">Данные строки, но не данные схемы сохраняется в строке.</span><span class="sxs-lookup"><span data-stu-id="19041-129">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="19041-130">Таким образом, **набор записей** не может быть открыт с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="19041-130">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="19041-131">Этот метод является эквивалентом метода RDO **GetClipString** .</span><span class="sxs-lookup"><span data-stu-id="19041-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


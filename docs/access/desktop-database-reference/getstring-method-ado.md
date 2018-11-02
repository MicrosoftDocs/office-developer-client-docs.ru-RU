---
title: Метод GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c6524c52ad3c4821d5b7987415f8a9c2dcb1b1d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919026"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="51bba-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="51bba-102">GetString method (ADO)</span></span>


<span data-ttu-id="51bba-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51bba-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="51bba-104">Возвращает [набор записей](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="51bba-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51bba-105">Syntax</span></span>

<span data-ttu-id="51bba-106">*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="51bba-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="51bba-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51bba-107">Return value</span></span>

<span data-ttu-id="51bba-108">Возвращает **набор записей** как строковое значение **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="51bba-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="51bba-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="51bba-109">Parameters</span></span>

  - <span data-ttu-id="51bba-110">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="51bba-110">*StringFormat*</span></span>

  - <span data-ttu-id="51bba-111">[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string.</span><span class="sxs-lookup"><span data-stu-id="51bba-111">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="51bba-112">Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="51bba-112">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="51bba-113">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="51bba-113">*NumRows*</span></span>

  - <span data-ttu-id="51bba-114">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="51bba-114">Optional.</span></span> <span data-ttu-id="51bba-115">Количество строк, преобразуется в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="51bba-115">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="51bba-116">Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="51bba-116">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="51bba-117">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="51bba-117">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="51bba-118">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="51bba-118">Optional.</span></span> <span data-ttu-id="51bba-119">Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="51bba-119">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="51bba-120">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="51bba-120">*RowDelimiter*</span></span>

  - <span data-ttu-id="51bba-121">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="51bba-121">Optional.</span></span> <span data-ttu-id="51bba-122">Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="51bba-122">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="51bba-123">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="51bba-123">*NullExpr*</span></span>

  - <span data-ttu-id="51bba-124">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="51bba-124">Optional.</span></span> <span data-ttu-id="51bba-125">Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="51bba-125">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="51bba-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="51bba-126">Remarks</span></span>

<span data-ttu-id="51bba-127">Данные строки, но не данные схемы сохраняется в строке.</span><span class="sxs-lookup"><span data-stu-id="51bba-127">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="51bba-128">Таким образом, **набор записей** не может быть открыт с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="51bba-128">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="51bba-129">Этот метод является эквивалентом метода RDO **GetClipString** .</span><span class="sxs-lookup"><span data-stu-id="51bba-129">This method is equivalent to the RDO **GetClipString** method.</span></span>


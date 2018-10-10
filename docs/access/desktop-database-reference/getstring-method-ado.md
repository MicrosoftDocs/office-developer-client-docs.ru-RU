---
title: GetString Method (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b11ddeb5a2cffad6ef7703b04d5730b54c4949b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481314"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="db036-102">GetString Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="db036-102">GetString Method (ADO)</span></span>


<span data-ttu-id="db036-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="db036-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="db036-104">Возвращает [набор записей](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="db036-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="db036-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db036-105">Syntax</span></span>

<span data-ttu-id="db036-106">*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="db036-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="db036-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db036-107">Return Value</span></span>

<span data-ttu-id="db036-108">Возвращает **набор записей** как строковое значение **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="db036-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="db036-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="db036-109">Parameters</span></span>

  - <span data-ttu-id="db036-110">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="db036-110">*StringFormat*</span></span>

  - <span data-ttu-id="db036-111">[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string.</span><span class="sxs-lookup"><span data-stu-id="db036-111">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="db036-112">Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="db036-112">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="db036-113">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="db036-113">*NumRows*</span></span>

  - <span data-ttu-id="db036-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="db036-114">Optional.</span></span> <span data-ttu-id="db036-115">Количество строк, преобразуется в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="db036-115">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="db036-116">Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="db036-116">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="db036-117">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="db036-117">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="db036-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="db036-118">Optional.</span></span> <span data-ttu-id="db036-119">Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="db036-119">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="db036-120">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="db036-120">*RowDelimiter*</span></span>

  - <span data-ttu-id="db036-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="db036-121">Optional.</span></span> <span data-ttu-id="db036-122">Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="db036-122">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="db036-123">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="db036-123">*NullExpr*</span></span>

  - <span data-ttu-id="db036-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="db036-124">Optional.</span></span> <span data-ttu-id="db036-125">Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="db036-125">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="db036-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="db036-126">Remarks</span></span>

<span data-ttu-id="db036-127">Данные строки, но не данные схемы сохраняется в строке.</span><span class="sxs-lookup"><span data-stu-id="db036-127">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="db036-128">Таким образом, **набор записей** не может быть открыт с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="db036-128">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="db036-129">Этот метод является эквивалентом метода RDO **GetClipString** .</span><span class="sxs-lookup"><span data-stu-id="db036-129">This method is equivalent to the RDO **GetClipString** method.</span></span>


---
title: GetString Method (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba235094aa7f491cbd86bf753713d50f01009d47
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605403"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="0aab2-102">GetString Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="0aab2-102">GetString Method (ADO)</span></span>


<span data-ttu-id="0aab2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0aab2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="0aab2-104">Возвращает [набор записей](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="0aab2-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aab2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0aab2-105">Syntax</span></span>

<span data-ttu-id="0aab2-106">*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="0aab2-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

<span data-ttu-id="0aab2-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0aab2-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0aab2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aab2-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0aab2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aab2-109">Return value</span></span>
>>>>>>> <span data-ttu-id="0aab2-110">master</span><span class="sxs-lookup"><span data-stu-id="0aab2-110">master</span></span>

<span data-ttu-id="0aab2-111">Возвращает **набор записей** как строковое значение **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="0aab2-111">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="0aab2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aab2-112">Parameters</span></span>

  - <span data-ttu-id="0aab2-113">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="0aab2-113">*StringFormat*</span></span>

  - <span data-ttu-id="0aab2-114">[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string.</span><span class="sxs-lookup"><span data-stu-id="0aab2-114">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="0aab2-115">Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="0aab2-115">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="0aab2-116">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="0aab2-116">*NumRows*</span></span>

  - <span data-ttu-id="0aab2-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0aab2-117">Optional.</span></span> <span data-ttu-id="0aab2-118">Количество строк, преобразуется в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="0aab2-118">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="0aab2-119">Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="0aab2-119">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="0aab2-120">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="0aab2-120">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="0aab2-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0aab2-121">Optional.</span></span> <span data-ttu-id="0aab2-122">Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="0aab2-122">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="0aab2-123">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="0aab2-123">*RowDelimiter*</span></span>

  - <span data-ttu-id="0aab2-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0aab2-124">Optional.</span></span> <span data-ttu-id="0aab2-125">Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="0aab2-125">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="0aab2-126">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="0aab2-126">*NullExpr*</span></span>

  - <span data-ttu-id="0aab2-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0aab2-127">Optional.</span></span> <span data-ttu-id="0aab2-128">Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="0aab2-128">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aab2-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="0aab2-129">Remarks</span></span>

<span data-ttu-id="0aab2-130">Данные строки, но не данные схемы сохраняется в строке.</span><span class="sxs-lookup"><span data-stu-id="0aab2-130">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="0aab2-131">Таким образом, **набор записей** не может быть открыт с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="0aab2-131">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="0aab2-132">Этот метод является эквивалентом метода RDO **GetClipString** .</span><span class="sxs-lookup"><span data-stu-id="0aab2-132">This method is equivalent to the RDO **GetClipString** method.</span></span>


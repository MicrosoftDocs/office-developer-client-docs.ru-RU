---
title: Метод GetString (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6c4de1278a093a1b0d4493c5dd994afe6a5d1b8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879874"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="48b9f-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="48b9f-102">GetString Method (ADO)</span></span>


<span data-ttu-id="48b9f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48b9f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="48b9f-104">Возвращает [набор записей](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="48b9f-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48b9f-105">Syntax</span></span>

<span data-ttu-id="48b9f-106">*Variant* = *набора записей*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="48b9f-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="48b9f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48b9f-107">Return value</span></span>

<span data-ttu-id="48b9f-108">Возвращает **набор записей** как строковое значение **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="48b9f-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="48b9f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="48b9f-109">Parameters</span></span>

  - <span data-ttu-id="48b9f-110">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="48b9f-110">*StringFormat*</span></span>

  - <span data-ttu-id="48b9f-111">[StringFormatEnum](stringformatenum.md) значение, указывающее, преобразование **набора записей** к типу string.</span><span class="sxs-lookup"><span data-stu-id="48b9f-111">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="48b9f-112">Параметры *RowDelimiter* *ColumnDelimiter*и *NullExpr* используются только с *StringFormat* из **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="48b9f-112">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="48b9f-113">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="48b9f-113">*NumRows*</span></span>

  - <span data-ttu-id="48b9f-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="48b9f-114">Optional.</span></span> <span data-ttu-id="48b9f-115">Количество строк, преобразуется в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="48b9f-115">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="48b9f-116">Если не указан *NumRows* или больше, чем общее число строк в **набор записей**, все строки в наборе **записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="48b9f-116">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="48b9f-117">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="48b9f-117">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="48b9f-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="48b9f-118">Optional.</span></span> <span data-ttu-id="48b9f-119">Разделитель, используемый между столбцов, если указан, в противном случае символ табуляции.</span><span class="sxs-lookup"><span data-stu-id="48b9f-119">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="48b9f-120">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="48b9f-120">*RowDelimiter*</span></span>

  - <span data-ttu-id="48b9f-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="48b9f-121">Optional.</span></span> <span data-ttu-id="48b9f-122">Разделитель, используемый между строк, если указан, в противном случае знаков возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="48b9f-122">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="48b9f-123">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="48b9f-123">*NullExpr*</span></span>

  - <span data-ttu-id="48b9f-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="48b9f-124">Optional.</span></span> <span data-ttu-id="48b9f-125">Выражение, используется вместо значение null, если указан, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="48b9f-125">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b9f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="48b9f-126">Remarks</span></span>

<span data-ttu-id="48b9f-127">Данные строки, но не данные схемы сохраняется в строке.</span><span class="sxs-lookup"><span data-stu-id="48b9f-127">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="48b9f-128">Таким образом, **набор записей** не может быть открыт с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="48b9f-128">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="48b9f-129">Этот метод является эквивалентом метода RDO **GetClipString** .</span><span class="sxs-lookup"><span data-stu-id="48b9f-129">This method is equivalent to the RDO **GetClipString** method.</span></span>


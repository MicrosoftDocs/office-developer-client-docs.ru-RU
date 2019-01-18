---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720963"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="74b6e-102">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="74b6e-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="74b6e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74b6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74b6e-104">Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="74b6e-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="74b6e-105">При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="74b6e-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="74b6e-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="74b6e-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74b6e-107">Syntax</span></span>

<span data-ttu-id="74b6e-108">HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="74b6e-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="74b6e-109">Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="74b6e-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="74b6e-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="74b6e-110">Parameters</span></span>

|<span data-ttu-id="74b6e-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="74b6e-111">Parameter</span></span>|<span data-ttu-id="74b6e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="74b6e-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="74b6e-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="74b6e-113">*ppRowPos*</span></span> |<span data-ttu-id="74b6e-114">Указатель на объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="74b6e-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="74b6e-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="74b6e-115">*PRowPos*</span></span> |<span data-ttu-id="74b6e-116">Объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="74b6e-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="74b6e-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="74b6e-117">Return values</span></span>

<span data-ttu-id="74b6e-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="74b6e-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b6e-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="74b6e-119">Remarks</span></span>

<span data-ttu-id="74b6e-120">Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй.</span><span class="sxs-lookup"><span data-stu-id="74b6e-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="74b6e-121">То же самое относится к текущей **главы** **RowPosition** также.</span><span class="sxs-lookup"><span data-stu-id="74b6e-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="74b6e-122">Область применения</span><span class="sxs-lookup"><span data-stu-id="74b6e-122">Applies to</span></span>

[<span data-ttu-id="74b6e-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="74b6e-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


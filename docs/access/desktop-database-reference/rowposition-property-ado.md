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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306862"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="1bef5-102">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="1bef5-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="1bef5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bef5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bef5-104">Получает или задает объект OLE DB **RowPosition** из/на **объект ADORecordsetConstruction.**</span><span class="sxs-lookup"><span data-stu-id="1bef5-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="1bef5-105">При использовании **put \_ RowPosition** для определения объекта **RowPosition** в результате объект **Recordset** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="1bef5-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="1bef5-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1bef5-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bef5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bef5-107">Syntax</span></span>

<span data-ttu-id="1bef5-108">HRESULT get \_ RowPosition \[ (out, retval \] IUnknown \* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="1bef5-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="1bef5-109">HRESULT put \_ RowPosition \[ (in \] IUnknown \* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="1bef5-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="1bef5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bef5-110">Parameters</span></span>

|<span data-ttu-id="1bef5-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="1bef5-111">Parameter</span></span>|<span data-ttu-id="1bef5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1bef5-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1bef5-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="1bef5-113">*ppRowPos*</span></span> |<span data-ttu-id="1bef5-114">Указатель на объект **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1bef5-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="1bef5-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="1bef5-115">*PRowPos*</span></span> |<span data-ttu-id="1bef5-116">Объект **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1bef5-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="1bef5-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1bef5-117">Return values</span></span>

<span data-ttu-id="1bef5-118">Этот метод свойства возвращает стандартные значения HRESULT, в том числе S \_ OK и E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="1bef5-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bef5-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bef5-119">Remarks</span></span>

<span data-ttu-id="1bef5-120">Если это свойство задано, если объект **Rowset** на объекте **RowPosition** отличается от объекта Rowset на объекте **Recordset,** первый переопределит последнее. </span><span class="sxs-lookup"><span data-stu-id="1bef5-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="1bef5-121">То же самое относится и к текущей **главе** **RowPosition.**</span><span class="sxs-lookup"><span data-stu-id="1bef5-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1bef5-122">Область применения</span><span class="sxs-lookup"><span data-stu-id="1bef5-122">Applies to</span></span>

[<span data-ttu-id="1bef5-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="1bef5-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


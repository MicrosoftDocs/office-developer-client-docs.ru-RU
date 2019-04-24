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
# <a name="rowposition-property-ado"></a><span data-ttu-id="33257-102">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="33257-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="33257-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33257-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33257-104">Получает или задает объект **ROWPOSITION** OLE DB from/On объекта **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="33257-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="33257-105">При использовании **Put\_RowPosition** для задания объекта **RowPosition** результирующий объект **Recordset** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="33257-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="33257-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="33257-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33257-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33257-107">Syntax</span></span>

<span data-ttu-id="33257-108">HRESULT Get\_RowPosition (\[out,\] IUnknown,\* \* IUnknown ппровпос);</span><span class="sxs-lookup"><span data-stu-id="33257-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="33257-109">HRESULT PUT\_RowPosition (\[в\] IUnknown\* провпос);</span><span class="sxs-lookup"><span data-stu-id="33257-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="33257-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="33257-110">Parameters</span></span>

|<span data-ttu-id="33257-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="33257-111">Parameter</span></span>|<span data-ttu-id="33257-112">Описание</span><span class="sxs-lookup"><span data-stu-id="33257-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="33257-113">*Ппровпос*</span><span class="sxs-lookup"><span data-stu-id="33257-113">*ppRowPos*</span></span> |<span data-ttu-id="33257-114">Указатель на объект **ROWPOSITION** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="33257-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="33257-115">*Провпос*</span><span class="sxs-lookup"><span data-stu-id="33257-115">*PRowPos*</span></span> |<span data-ttu-id="33257-116">Объект **ROWPOSITION** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="33257-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="33257-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="33257-117">Return values</span></span>

<span data-ttu-id="33257-118">Этот метод свойства возвращает стандартные значения HRESULT, включая S\_ОК и электронную\_ошибку.</span><span class="sxs-lookup"><span data-stu-id="33257-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="33257-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="33257-119">Remarks</span></span>

<span data-ttu-id="33257-120">Если это свойство задано, то в случае, если объект **набора строк** в объекте **RowPosition** отличается от объекта набора **строк** в объекте **Recordset** , прежний приоритет переопределяется последним.</span><span class="sxs-lookup"><span data-stu-id="33257-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="33257-121">Такое же поведение распространяется и на текущую **главу** **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="33257-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="33257-122">Область применения</span><span class="sxs-lookup"><span data-stu-id="33257-122">Applies to</span></span>

[<span data-ttu-id="33257-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="33257-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


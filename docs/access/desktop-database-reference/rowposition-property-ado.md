---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0adb1cdf9ce7b096d7b80b86a89a819d5789b60b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949385"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="c3d70-102">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="c3d70-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="c3d70-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3d70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3d70-104">Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="c3d70-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="c3d70-105">При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="c3d70-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="c3d70-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c3d70-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3d70-107">Syntax</span></span>

<span data-ttu-id="c3d70-108">HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="c3d70-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="c3d70-109">Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="c3d70-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="c3d70-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d70-110">Parameters</span></span>

|<span data-ttu-id="c3d70-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="c3d70-111">Parameter</span></span>|<span data-ttu-id="c3d70-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c3d70-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c3d70-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="c3d70-113">*ppRowPos*</span></span> |<span data-ttu-id="c3d70-114">Указатель на объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="c3d70-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="c3d70-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="c3d70-115">*PRowPos*</span></span> |<span data-ttu-id="c3d70-116">Объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="c3d70-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="c3d70-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c3d70-117">Return values</span></span>

<span data-ttu-id="c3d70-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="c3d70-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d70-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3d70-119">Remarks</span></span>

<span data-ttu-id="c3d70-120">Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй.</span><span class="sxs-lookup"><span data-stu-id="c3d70-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="c3d70-121">То же самое относится к текущей **главы** **RowPosition** также.</span><span class="sxs-lookup"><span data-stu-id="c3d70-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3d70-122">Область применения</span><span class="sxs-lookup"><span data-stu-id="c3d70-122">Applies to</span></span>

[<span data-ttu-id="c3d70-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="c3d70-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


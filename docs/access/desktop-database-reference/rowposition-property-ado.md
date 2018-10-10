---
title: RowPosition Property (ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480648"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="ca6a1-102">RowPosition Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca6a1-102">RowPosition Property (ADO)</span></span>


<span data-ttu-id="ca6a1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca6a1-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ca6a1-104">Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="ca6a1-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="ca6a1-105">При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="ca6a1-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="ca6a1-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ca6a1-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca6a1-107">Syntax</span></span>

<span data-ttu-id="ca6a1-108">HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="ca6a1-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="ca6a1-109">Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="ca6a1-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="ca6a1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca6a1-110">Parameters</span></span>

  - <span data-ttu-id="ca6a1-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="ca6a1-111">*ppRowPos*</span></span>

  - <span data-ttu-id="ca6a1-112">Указатель на объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="ca6a1-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="ca6a1-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="ca6a1-113">*PRowPos*</span></span>

  - <span data-ttu-id="ca6a1-114">Объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="ca6a1-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca6a1-115">Return Values</span><span class="sxs-lookup"><span data-stu-id="ca6a1-115">Return Values</span></span>

<span data-ttu-id="ca6a1-116">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="ca6a1-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca6a1-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca6a1-117">Remarks</span></span>

<span data-ttu-id="ca6a1-118">Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй.</span><span class="sxs-lookup"><span data-stu-id="ca6a1-118">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="ca6a1-119">То же самое относится к текущей **главы** **RowPosition** также.</span><span class="sxs-lookup"><span data-stu-id="ca6a1-119">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ca6a1-120">Применимо к</span><span class="sxs-lookup"><span data-stu-id="ca6a1-120">Applies To</span></span>

[<span data-ttu-id="ca6a1-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="ca6a1-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


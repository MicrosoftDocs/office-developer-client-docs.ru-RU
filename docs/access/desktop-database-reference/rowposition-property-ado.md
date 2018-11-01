---
title: Свойство RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869073"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="9e406-102">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e406-102">RowPosition property (ADO)</span></span>


<span data-ttu-id="9e406-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e406-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="9e406-104">Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="9e406-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="9e406-105">При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="9e406-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="9e406-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9e406-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e406-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e406-107">Syntax</span></span>

<span data-ttu-id="9e406-108">HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="9e406-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="9e406-109">Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="9e406-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="9e406-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e406-110">Parameters</span></span>

  - <span data-ttu-id="9e406-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="9e406-111">*ppRowPos*</span></span>

  - <span data-ttu-id="9e406-112">Указатель на объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="9e406-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="9e406-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="9e406-113">*PRowPos*</span></span>

  - <span data-ttu-id="9e406-114">Объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="9e406-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e406-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9e406-115">Return values</span></span>

<span data-ttu-id="9e406-116">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="9e406-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e406-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e406-117">Remarks</span></span>

<span data-ttu-id="9e406-118">Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй.</span><span class="sxs-lookup"><span data-stu-id="9e406-118">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="9e406-119">То же самое относится к текущей **главы** **RowPosition** также.</span><span class="sxs-lookup"><span data-stu-id="9e406-119">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e406-120">Применимо к</span><span class="sxs-lookup"><span data-stu-id="9e406-120">Applies To</span></span>

[<span data-ttu-id="9e406-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="9e406-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


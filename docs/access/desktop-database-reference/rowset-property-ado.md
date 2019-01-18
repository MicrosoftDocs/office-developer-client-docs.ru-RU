---
title: Свойство Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706144"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="8c2d1-102">Свойство Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c2d1-102">Rowset property (ADO)</span></span>

<span data-ttu-id="8c2d1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c2d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c2d1-104">Получает или задает объект OLE DB **строк** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="8c2d1-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="8c2d1-105">При использовании put\_включается набор строк, набор строк, в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="8c2d1-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="8c2d1-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8c2d1-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2d1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c2d1-107">Syntax</span></span>

<span data-ttu-id="8c2d1-108">HRESULT get\_набор строк (\[out retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="8c2d1-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="8c2d1-109">Поместите HRESULT\_набор строк (\[в\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="8c2d1-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="8c2d1-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="8c2d1-110">Parameters</span></span>

|<span data-ttu-id="8c2d1-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="8c2d1-111">Parameter</span></span>|<span data-ttu-id="8c2d1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8c2d1-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8c2d1-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="8c2d1-113">*ppRowset*</span></span> |<span data-ttu-id="8c2d1-114">Указатель на объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="8c2d1-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="8c2d1-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="8c2d1-115">*PRowset*</span></span> |<span data-ttu-id="8c2d1-116">Объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="8c2d1-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="8c2d1-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8c2d1-117">Return values</span></span>

<span data-ttu-id="8c2d1-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="8c2d1-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8c2d1-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="8c2d1-119">Applies to</span></span>

[<span data-ttu-id="8c2d1-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="8c2d1-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


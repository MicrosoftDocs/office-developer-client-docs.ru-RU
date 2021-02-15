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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306743"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="ae969-102">Свойство Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="ae969-102">Rowset property (ADO)</span></span>

<span data-ttu-id="ae969-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae969-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae969-104">Получает или задает объект OLE DB **Rowset** из/объекта **ADORecordsetConstruction.**</span><span class="sxs-lookup"><span data-stu-id="ae969-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="ae969-105">При использовании put \_ Rowset набор строк превращается в объект ADO **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ae969-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="ae969-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ae969-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae969-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae969-107">Syntax</span></span>

<span data-ttu-id="ae969-108">HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="ae969-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="ae969-109">HRESULT put \_ Rowset( \[ in \] IUnknown \* pRowset);</span><span class="sxs-lookup"><span data-stu-id="ae969-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="ae969-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae969-110">Parameters</span></span>

|<span data-ttu-id="ae969-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="ae969-111">Parameter</span></span>|<span data-ttu-id="ae969-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ae969-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ae969-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="ae969-113">*ppRowset*</span></span> |<span data-ttu-id="ae969-114">Указатель на объект **rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ae969-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="ae969-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="ae969-115">*PRowset*</span></span> |<span data-ttu-id="ae969-116">Объект OLE DB **Rowset.**</span><span class="sxs-lookup"><span data-stu-id="ae969-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="ae969-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae969-117">Return values</span></span>

<span data-ttu-id="ae969-118">Этот метод свойства возвращает стандартные значения HRESULT, включая S \_ OK и E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="ae969-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ae969-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="ae969-119">Applies to</span></span>

[<span data-ttu-id="ae969-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="ae969-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


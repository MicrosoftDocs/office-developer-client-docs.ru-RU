---
title: Свойство Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949791"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="38e43-102">Свойство Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="38e43-102">Rowset property (ADO)</span></span>

<span data-ttu-id="38e43-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38e43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38e43-104">Получает или задает объект OLE DB **строк** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="38e43-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="38e43-105">При использовании put\_включается набор строк, набор строк, в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="38e43-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="38e43-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="38e43-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38e43-107">Syntax</span></span>

<span data-ttu-id="38e43-108">HRESULT get\_набор строк (\[out retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="38e43-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="38e43-109">Поместите HRESULT\_набор строк (\[в\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="38e43-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="38e43-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="38e43-110">Parameters</span></span>

|<span data-ttu-id="38e43-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="38e43-111">Parameter</span></span>|<span data-ttu-id="38e43-112">Описание</span><span class="sxs-lookup"><span data-stu-id="38e43-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="38e43-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="38e43-113">*ppRowset*</span></span> |<span data-ttu-id="38e43-114">Указатель на объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="38e43-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="38e43-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="38e43-115">*PRowset*</span></span> |<span data-ttu-id="38e43-116">Объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="38e43-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="38e43-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="38e43-117">Return values</span></span>

<span data-ttu-id="38e43-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="38e43-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="38e43-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="38e43-119">Applies to</span></span>

[<span data-ttu-id="38e43-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="38e43-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


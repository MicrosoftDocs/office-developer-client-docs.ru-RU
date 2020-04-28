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
# <a name="rowset-property-ado"></a><span data-ttu-id="f4231-102">Свойство Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="f4231-102">Rowset property (ADO)</span></span>

<span data-ttu-id="f4231-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4231-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4231-104">Получает или задает объект **набора строк** OLE DB from/On объекта **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="f4231-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f4231-105">При использовании параметра PUT\_набор строк включается в объект **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="f4231-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="f4231-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f4231-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4231-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4231-107">Syntax</span></span>

<span data-ttu-id="f4231-108">HRESULT Get\_Rowset (\[out,\] IUnknown IUnknown\* \* ппровсет);</span><span class="sxs-lookup"><span data-stu-id="f4231-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="f4231-109">HRESULT PUT\_Rowset (\[в\] интерфейсе IUnknown\* провсет);</span><span class="sxs-lookup"><span data-stu-id="f4231-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="f4231-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4231-110">Parameters</span></span>

|<span data-ttu-id="f4231-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="f4231-111">Parameter</span></span>|<span data-ttu-id="f4231-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f4231-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f4231-113">*ппровсет*</span><span class="sxs-lookup"><span data-stu-id="f4231-113">*ppRowset*</span></span> |<span data-ttu-id="f4231-114">Указатель на объект **набора строк** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f4231-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="f4231-115">*провсет*</span><span class="sxs-lookup"><span data-stu-id="f4231-115">*PRowset*</span></span> |<span data-ttu-id="f4231-116">Объект **набора строк** в OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f4231-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f4231-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f4231-117">Return values</span></span>

<span data-ttu-id="f4231-118">Этот метод свойства возвращает стандартные значения HRESULT, включая S\_ОК и электронную\_ошибку.</span><span class="sxs-lookup"><span data-stu-id="f4231-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4231-119">Сфера применения</span><span class="sxs-lookup"><span data-stu-id="f4231-119">Applies to</span></span>

[<span data-ttu-id="f4231-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f4231-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


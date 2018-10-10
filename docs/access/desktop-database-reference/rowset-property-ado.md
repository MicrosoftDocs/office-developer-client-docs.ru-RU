---
title: Rowset Property (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481481"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="bfdde-102">Rowset Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="bfdde-102">Rowset Property (ADO)</span></span>


<span data-ttu-id="bfdde-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfdde-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="bfdde-104">Получает или задает объект OLE DB **строк** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="bfdde-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="bfdde-105">При использовании put\_включается набор строк, набор строк, в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="bfdde-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="bfdde-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bfdde-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdde-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfdde-107">Syntax</span></span>

<span data-ttu-id="bfdde-108">HRESULT get\_набор строк (\[out retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="bfdde-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="bfdde-109">Поместите HRESULT\_набор строк (\[в\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="bfdde-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="bfdde-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfdde-110">Parameters</span></span>

  - <span data-ttu-id="bfdde-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="bfdde-111">*ppRowset*</span></span>

  - <span data-ttu-id="bfdde-112">Указатель на объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="bfdde-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="bfdde-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="bfdde-113">*PRowset*</span></span>

  - <span data-ttu-id="bfdde-114">Объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="bfdde-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="bfdde-115">Return Values</span><span class="sxs-lookup"><span data-stu-id="bfdde-115">Return Values</span></span>

<span data-ttu-id="bfdde-116">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="bfdde-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="bfdde-117">Применимо к</span><span class="sxs-lookup"><span data-stu-id="bfdde-117">Applies To</span></span>

[<span data-ttu-id="bfdde-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="bfdde-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


---
title: Свойство Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717939"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="38a6f-102">Свойство Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="38a6f-102">Chapter property (ADO)</span></span>

<span data-ttu-id="38a6f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38a6f-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="38a6f-104">Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="38a6f-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="38a6f-105">При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="38a6f-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="38a6f-106">Это задание текущей главы из объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="38a6f-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="38a6f-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="38a6f-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a6f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a6f-108">Syntax</span></span>

<span data-ttu-id="38a6f-109">HRESULT get\_главы (\[out retval\] длинные\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="38a6f-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="38a6f-110">Поместите HRESULT\_главы (\[в\] длинные lChapter);</span><span class="sxs-lookup"><span data-stu-id="38a6f-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="38a6f-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="38a6f-111">Parameters</span></span>

|<span data-ttu-id="38a6f-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="38a6f-112">Parameter</span></span>|<span data-ttu-id="38a6f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="38a6f-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="38a6f-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="38a6f-114">*plChapter*</span></span> |<span data-ttu-id="38a6f-115">Указатель на дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="38a6f-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="38a6f-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="38a6f-116">*LChapter*</span></span> |<span data-ttu-id="38a6f-117">Дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="38a6f-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="38a6f-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="38a6f-118">Return values</span></span>

<span data-ttu-id="38a6f-119">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="38a6f-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="38a6f-120">Применимо к</span><span class="sxs-lookup"><span data-stu-id="38a6f-120">Applies To</span></span>

[<span data-ttu-id="38a6f-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="38a6f-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


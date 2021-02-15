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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296397"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="42184-102">Свойство Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="42184-102">Chapter property (ADO)</span></span>

<span data-ttu-id="42184-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42184-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="42184-104">Получает или задает объект главы OLE DB **из/объекта** **ADORecordsetConstruction.**</span><span class="sxs-lookup"><span data-stu-id="42184-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="42184-105">При использовании **put \_ Chapter** для применения объекта **Chapter** подмножество строк превращается в объект ADO **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="42184-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="42184-106">Это задает текущую главу объекта **Rowset.**</span><span class="sxs-lookup"><span data-stu-id="42184-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="42184-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="42184-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="42184-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42184-108">Syntax</span></span>

<span data-ttu-id="42184-109">HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);</span><span class="sxs-lookup"><span data-stu-id="42184-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="42184-110">HRESULT put \_ Chapter( \[ in long \] lChapter);</span><span class="sxs-lookup"><span data-stu-id="42184-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="42184-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="42184-111">Parameters</span></span>

|<span data-ttu-id="42184-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="42184-112">Parameter</span></span>|<span data-ttu-id="42184-113">Описание</span><span class="sxs-lookup"><span data-stu-id="42184-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="42184-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="42184-114">*plChapter*</span></span> |<span data-ttu-id="42184-115">Указатель на ладную часть главы.</span><span class="sxs-lookup"><span data-stu-id="42184-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="42184-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="42184-116">*LChapter*</span></span> |<span data-ttu-id="42184-117">Обработка главы.</span><span class="sxs-lookup"><span data-stu-id="42184-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="42184-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="42184-118">Return values</span></span>

<span data-ttu-id="42184-119">Этот метод свойства возвращает стандартные значения HRESULT, включая S \_ OK и E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="42184-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="42184-120">Применимость</span><span class="sxs-lookup"><span data-stu-id="42184-120">Applies To</span></span>

[<span data-ttu-id="42184-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="42184-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


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
# <a name="chapter-property-ado"></a><span data-ttu-id="2b848-102">Свойство Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="2b848-102">Chapter property (ADO)</span></span>

<span data-ttu-id="2b848-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b848-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="2b848-104">Получает или задает объект **главы** OLE DB from/On объекта **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="2b848-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="2b848-105">При использовании оператора **Put\_** для установки объекта **Chapter** подмножество строк включается в объект **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="2b848-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="2b848-106">В этом поле задается текущая глава объекта **набора строк** .</span><span class="sxs-lookup"><span data-stu-id="2b848-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="2b848-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2b848-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b848-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b848-108">Syntax</span></span>

<span data-ttu-id="2b848-109">HRESULT Get\_Chapter (\[out, retval\] Long\* плчаптер);</span><span class="sxs-lookup"><span data-stu-id="2b848-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="2b848-110">Раздел HRESULT\_put (\[в\] длинном лчаптер);</span><span class="sxs-lookup"><span data-stu-id="2b848-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="2b848-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b848-111">Parameters</span></span>

|<span data-ttu-id="2b848-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="2b848-112">Parameter</span></span>|<span data-ttu-id="2b848-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2b848-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2b848-114">*Плчаптер*</span><span class="sxs-lookup"><span data-stu-id="2b848-114">*plChapter*</span></span> |<span data-ttu-id="2b848-115">Указатель на маркер главы.</span><span class="sxs-lookup"><span data-stu-id="2b848-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="2b848-116">*Лчаптер*</span><span class="sxs-lookup"><span data-stu-id="2b848-116">*LChapter*</span></span> |<span data-ttu-id="2b848-117">Маркер главы.</span><span class="sxs-lookup"><span data-stu-id="2b848-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="2b848-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2b848-118">Return values</span></span>

<span data-ttu-id="2b848-119">Этот метод свойства возвращает стандартные значения HRESULT, включая S\_ОК и электронную\_ошибку.</span><span class="sxs-lookup"><span data-stu-id="2b848-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2b848-120">Применимость</span><span class="sxs-lookup"><span data-stu-id="2b848-120">Applies To</span></span>

[<span data-ttu-id="2b848-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="2b848-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


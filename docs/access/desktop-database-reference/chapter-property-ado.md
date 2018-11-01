---
title: Свойство Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eeb3c6e2e8c7b7f1c0f6e733c1b86545a5e954f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887826"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="31113-102">Свойство Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="31113-102">Chapter property (ADO)</span></span>


<span data-ttu-id="31113-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31113-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="31113-104">Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="31113-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="31113-105">При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="31113-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="31113-106">Это задание текущей главы из объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="31113-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="31113-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="31113-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31113-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31113-108">Syntax</span></span>

<span data-ttu-id="31113-109">HRESULT get\_главы (\[out retval\] длинные\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="31113-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="31113-110">Поместите HRESULT\_главы (\[в\] длинные lChapter);</span><span class="sxs-lookup"><span data-stu-id="31113-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="31113-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="31113-111">Parameters</span></span>

  - <span data-ttu-id="31113-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="31113-112">*plChapter*</span></span>

  - <span data-ttu-id="31113-113">Указатель на дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="31113-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="31113-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="31113-114">*LChapter*</span></span>

  - <span data-ttu-id="31113-115">Дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="31113-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="31113-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="31113-116">Return values</span></span>

<span data-ttu-id="31113-117">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="31113-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="31113-118">Применимо к</span><span class="sxs-lookup"><span data-stu-id="31113-118">Applies To</span></span>

[<span data-ttu-id="31113-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="31113-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


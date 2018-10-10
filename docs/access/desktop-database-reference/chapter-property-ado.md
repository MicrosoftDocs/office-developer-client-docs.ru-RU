---
title: Chapter Property (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482343"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="01b13-102">Chapter Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="01b13-102">Chapter Property (ADO)</span></span>


<span data-ttu-id="01b13-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01b13-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="01b13-104">Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="01b13-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="01b13-105">При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="01b13-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="01b13-106">Это задание текущей главы из объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="01b13-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="01b13-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="01b13-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b13-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01b13-108">Syntax</span></span>

<span data-ttu-id="01b13-109">HRESULT get\_главы (\[out retval\] длинные\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="01b13-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="01b13-110">Поместите HRESULT\_главы (\[в\] длинные lChapter);</span><span class="sxs-lookup"><span data-stu-id="01b13-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="01b13-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="01b13-111">Parameters</span></span>

  - <span data-ttu-id="01b13-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="01b13-112">*plChapter*</span></span>

  - <span data-ttu-id="01b13-113">Указатель на дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="01b13-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="01b13-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="01b13-114">*LChapter*</span></span>

  - <span data-ttu-id="01b13-115">Дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="01b13-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="01b13-116">Return Values</span><span class="sxs-lookup"><span data-stu-id="01b13-116">Return Values</span></span>

<span data-ttu-id="01b13-117">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="01b13-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="01b13-118">Применимо к</span><span class="sxs-lookup"><span data-stu-id="01b13-118">Applies To</span></span>

[<span data-ttu-id="01b13-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="01b13-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


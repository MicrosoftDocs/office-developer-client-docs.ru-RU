---
title: Свойство Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95ed1b9b7c048353950b2481c7fefe2211b2799b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944279"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="59722-102">Свойство Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="59722-102">Chapter property (ADO)</span></span>


<span data-ttu-id="59722-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59722-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="59722-104">Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="59722-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="59722-105">При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="59722-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="59722-106">Это задание текущей главы из объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="59722-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="59722-107">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="59722-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59722-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59722-108">Syntax</span></span>

<span data-ttu-id="59722-109">HRESULT get\_главы (\[out retval\] длинные\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="59722-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="59722-110">Поместите HRESULT\_главы (\[в\] длинные lChapter);</span><span class="sxs-lookup"><span data-stu-id="59722-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="59722-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="59722-111">Parameters</span></span>

- <span data-ttu-id="59722-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="59722-112">*plChapter*</span></span>

  - <span data-ttu-id="59722-113">Указатель на дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="59722-113">Pointer to the handle of a chapter.</span></span>

- <span data-ttu-id="59722-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="59722-114">*LChapter*</span></span>

  - <span data-ttu-id="59722-115">Дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="59722-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="59722-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59722-116">Return values</span></span>

<span data-ttu-id="59722-117">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="59722-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="59722-118">Применимо к</span><span class="sxs-lookup"><span data-stu-id="59722-118">Applies To</span></span>

[<span data-ttu-id="59722-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="59722-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


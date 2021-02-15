---
title: Событие FetchProgress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293184"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="2b942-102">Событие FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="2b942-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="2b942-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b942-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b942-104">Событие **FetchProgress** периодически вызвано во время продолжительной асинхронной операции, чтобы сообщить, сколько еще строк в данный момент было извлечено в [набор recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2b942-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b942-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b942-105">Syntax</span></span>

<span data-ttu-id="2b942-106">FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2b942-106">FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="2b942-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b942-107">Parameters</span></span>

|<span data-ttu-id="2b942-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2b942-108">Parameter</span></span>|<span data-ttu-id="2b942-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2b942-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2b942-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="2b942-110">*Progress*</span></span> |<span data-ttu-id="2b942-111">**Длинное** значение, указывающее количество записей, которые в настоящее время были извлечены операцией получения.</span><span class="sxs-lookup"><span data-stu-id="2b942-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="2b942-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="2b942-112">*MaxProgress*</span></span> |<span data-ttu-id="2b942-113">**Длинное** значение, указывающее максимальное число записей, которые должны быть извлечены.</span><span class="sxs-lookup"><span data-stu-id="2b942-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="2b942-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="2b942-114">*adStatus*</span></span> |<span data-ttu-id="2b942-115">Значение [состояния EventStatusEnum.](eventstatusenum.md)</span><span class="sxs-lookup"><span data-stu-id="2b942-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="2b942-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2b942-116">*pRecordset*</span></span> |<span data-ttu-id="2b942-117">Объект **Recordset,** который является объектом, для которого извлекаются записи.</span><span class="sxs-lookup"><span data-stu-id="2b942-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2b942-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="2b942-118">Remarks</span></span>

<span data-ttu-id="2b942-119">При использовании **FetchProgress** с другим набором записей следует **помнить,** что значения параметров *Progress* и *MaxProgress* являются производными от используемой строки [cursor Service.](microsoft-cursor-service-for-ole-db-ado-service-component.md)</span><span class="sxs-lookup"><span data-stu-id="2b942-119">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="2b942-120">Возвращаемые значения представляют общее число записей в основном наборе строк, а не только количество записей в текущей главе.</span><span class="sxs-lookup"><span data-stu-id="2b942-120">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="2b942-121">Чтобы использовать **FetchProgress** с Microsoft Visual Basic, Visual Basic 6.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2b942-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>



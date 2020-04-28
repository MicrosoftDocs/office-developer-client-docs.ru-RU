---
title: Событие событие fetchprogress (ADO)
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
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="77226-102">Событие событие fetchprogress (ADO)</span><span class="sxs-lookup"><span data-stu-id="77226-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="77226-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77226-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77226-104">Событие **событие fetchprogress** вызывается периодически в течение длительной асинхронной операции, чтобы сообщить, сколько строк в данный момент было извлечено в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="77226-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77226-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77226-105">Syntax</span></span>

<span data-ttu-id="77226-106">*Ход выполнения*событие fetchprogress, *макспрогресс*, адстатус *,* пред *adStatus*</span><span class="sxs-lookup"><span data-stu-id="77226-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="77226-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77226-107">Parameters</span></span>

|<span data-ttu-id="77226-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="77226-108">Parameter</span></span>|<span data-ttu-id="77226-109">Описание</span><span class="sxs-lookup"><span data-stu-id="77226-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="77226-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="77226-110">*Progress*</span></span> |<span data-ttu-id="77226-111">**Длинное** значение, указывающее количество записей, которые в настоящее время были получены операцией выборки.</span><span class="sxs-lookup"><span data-stu-id="77226-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="77226-112">*макспрогресс*</span><span class="sxs-lookup"><span data-stu-id="77226-112">*MaxProgress*</span></span> |<span data-ttu-id="77226-113">**Длинное** значение, указывающее максимальное количество получаемых записей.</span><span class="sxs-lookup"><span data-stu-id="77226-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="77226-114">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="77226-114">*adStatus*</span></span> |<span data-ttu-id="77226-115">Значение состояния [евентстатусенум](eventstatusenum.md) .</span><span class="sxs-lookup"><span data-stu-id="77226-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="77226-116">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="77226-116">*pRecordset*</span></span> |<span data-ttu-id="77226-117">Объект **Recordset** , представляющий собой объект, для которого извлекаются записи.</span><span class="sxs-lookup"><span data-stu-id="77226-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="77226-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="77226-118">Remarks</span></span>

<span data-ttu-id="77226-119">При использовании **событие fetchprogress** с дочерним объектом **Recordset**имейте в виду, что значения параметров *Progress* и *макспрогресс* являются производными от базового набора строк [службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="77226-119">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="77226-120">Возвращаемые значения представляют общее число записей в базовом наборе строк, а не только число записей в текущей главе.</span><span class="sxs-lookup"><span data-stu-id="77226-120">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="77226-121">Чтобы использовать **событие fetchprogress** с Microsoft Visual Basic, требуется Visual Basic 6,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77226-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>



---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edb2eefd36aea9f037ea4ad6afc51e0da18b76db
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945637"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="dafb7-102">Событие FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="dafb7-102">FetchComplete event (ADO)</span></span>


<span data-ttu-id="dafb7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dafb7-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="dafb7-104">Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dafb7-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dafb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dafb7-105">Syntax</span></span>

<span data-ttu-id="dafb7-106">FetchComplete*pError*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="dafb7-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="dafb7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dafb7-107">Parameters</span></span>

- <span data-ttu-id="dafb7-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="dafb7-108">*pError*</span></span>

  - <span data-ttu-id="dafb7-109">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dafb7-109">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="dafb7-110">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="dafb7-110">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

- <span data-ttu-id="dafb7-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="dafb7-111">*adStatus*</span></span>

  - [<span data-ttu-id="dafb7-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="dafb7-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="dafb7-113">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="dafb7-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

- <span data-ttu-id="dafb7-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="dafb7-114">*pRecordset*</span></span>

  - <span data-ttu-id="dafb7-115">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="dafb7-115">A **Recordset** object.</span></span> <span data-ttu-id="dafb7-116">Объект, для которого возвращенных записей.</span><span class="sxs-lookup"><span data-stu-id="dafb7-116">The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="dafb7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dafb7-117">Remarks</span></span>

<span data-ttu-id="dafb7-118">Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dafb7-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae09ff9bfcd694214a63fb630de52260ea7ac31
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925229"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="35e28-102">Событие FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="35e28-102">FetchComplete event (ADO)</span></span>


<span data-ttu-id="35e28-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35e28-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="35e28-104">Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="35e28-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35e28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35e28-105">Syntax</span></span>

<span data-ttu-id="35e28-106">FetchComplete*pError*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="35e28-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="35e28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35e28-107">Parameters</span></span>

  - <span data-ttu-id="35e28-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="35e28-108">*pError*</span></span>

  - <span data-ttu-id="35e28-109">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="35e28-109">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="35e28-110">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="35e28-110">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="35e28-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="35e28-111">*adStatus*</span></span>

  - [<span data-ttu-id="35e28-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="35e28-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="35e28-113">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="35e28-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="35e28-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="35e28-114">*pRecordset*</span></span>

  - <span data-ttu-id="35e28-115">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="35e28-115">A **Recordset** object.</span></span> <span data-ttu-id="35e28-116">Объект, для которого возвращенных записей.</span><span class="sxs-lookup"><span data-stu-id="35e28-116">The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e28-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="35e28-117">Remarks</span></span>

<span data-ttu-id="35e28-118">Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="35e28-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


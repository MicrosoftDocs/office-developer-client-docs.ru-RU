---
title: Событие FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a898ad02d551e0c4de02597761ccd3076fc5eb77
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862282"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="45ca2-102">Событие FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="45ca2-102">FetchProgress Event (ADO)</span></span>


<span data-ttu-id="45ca2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45ca2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="45ca2-104">Событие **FetchProgress** вызывается периодически во время длительных асинхронной операции для отчета, сколько увеличение количества строк в настоящее время извлечения в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="45ca2-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45ca2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45ca2-105">Syntax</span></span>

<span data-ttu-id="45ca2-106">FetchProgress*о ходе выполнения*, *MaxProgress* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="45ca2-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="45ca2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="45ca2-107">Parameters</span></span>

  - <span data-ttu-id="45ca2-108">*Ход выполнения*</span><span class="sxs-lookup"><span data-stu-id="45ca2-108">*Progress*</span></span>

  - <span data-ttu-id="45ca2-109">**Длинное** значение, указывающее количество записей, которые в настоящее время извлечения с операции выборки.</span><span class="sxs-lookup"><span data-stu-id="45ca2-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

  - <span data-ttu-id="45ca2-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="45ca2-110">*MaxProgress*</span></span>

  - <span data-ttu-id="45ca2-111">Значение типа **Long** , указывающее максимальное число записей должен извлечь.</span><span class="sxs-lookup"><span data-stu-id="45ca2-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

  - <span data-ttu-id="45ca2-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="45ca2-112">*adStatus*</span></span>

  - <span data-ttu-id="45ca2-113">Значение состояния [EventStatusEnum](eventstatusenum.md) .</span><span class="sxs-lookup"><span data-stu-id="45ca2-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

  - <span data-ttu-id="45ca2-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="45ca2-114">*pRecordset*</span></span>

  - <span data-ttu-id="45ca2-115">Объект **набора записей** , — это объект, для которого извлекаются записи.</span><span class="sxs-lookup"><span data-stu-id="45ca2-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ca2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="45ca2-116">Remarks</span></span>

<span data-ttu-id="45ca2-117">При использовании **FetchProgress** с дочерним **записей**, обратите внимание, что значение параметра *хода выполнения* и *MaxProgress* являются производными от в базовом наборе строк [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="45ca2-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="45ca2-118">Возвращаемые значения представляют общее число записей в базовом наборе строк, не только число записей в текущем.</span><span class="sxs-lookup"><span data-stu-id="45ca2-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="45ca2-119">Чтобы использовать **FetchProgress** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="45ca2-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>



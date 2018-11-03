---
title: Событие FetchProgress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44e41c3e9d46c9d26f5aed18755c158a5dc68ba7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946393"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="1864d-102">Событие FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="1864d-102">FetchProgress event (ADO)</span></span>


<span data-ttu-id="1864d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1864d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1864d-104">Событие **FetchProgress** вызывается периодически во время длительных асинхронной операции для отчета, сколько увеличение количества строк в настоящее время извлечения в [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1864d-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1864d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1864d-105">Syntax</span></span>

<span data-ttu-id="1864d-106">FetchProgress*о ходе выполнения*, *MaxProgress* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1864d-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1864d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1864d-107">Parameters</span></span>

- <span data-ttu-id="1864d-108">*Ход выполнения*</span><span class="sxs-lookup"><span data-stu-id="1864d-108">*Progress*</span></span>

  - <span data-ttu-id="1864d-109">**Длинное** значение, указывающее количество записей, которые в настоящее время извлечения с операции выборки.</span><span class="sxs-lookup"><span data-stu-id="1864d-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

- <span data-ttu-id="1864d-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="1864d-110">*MaxProgress*</span></span>

  - <span data-ttu-id="1864d-111">Значение типа **Long** , указывающее максимальное число записей должен извлечь.</span><span class="sxs-lookup"><span data-stu-id="1864d-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

- <span data-ttu-id="1864d-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1864d-112">*adStatus*</span></span>

  - <span data-ttu-id="1864d-113">Значение состояния [EventStatusEnum](eventstatusenum.md) .</span><span class="sxs-lookup"><span data-stu-id="1864d-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

- <span data-ttu-id="1864d-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1864d-114">*pRecordset*</span></span>

  - <span data-ttu-id="1864d-115">Объект **набора записей** , — это объект, для которого извлекаются записи.</span><span class="sxs-lookup"><span data-stu-id="1864d-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="1864d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1864d-116">Remarks</span></span>

<span data-ttu-id="1864d-117">При использовании **FetchProgress** с дочерним **записей**, обратите внимание, что значение параметра *хода выполнения* и *MaxProgress* являются производными от в базовом наборе строк [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="1864d-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="1864d-118">Возвращаемые значения представляют общее число записей в базовом наборе строк, не только число записей в текущем.</span><span class="sxs-lookup"><span data-stu-id="1864d-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="1864d-119">Чтобы использовать **FetchProgress** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1864d-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>



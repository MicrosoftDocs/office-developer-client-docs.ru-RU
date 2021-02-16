---
title: Функции соединители кластера Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408588"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="4acd6-103">Функции соединители кластера Excel</span><span class="sxs-lookup"><span data-stu-id="4acd6-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="4acd6-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4acd6-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4acd6-105">DLL соединителя кластера Microsoft Excel 2013 должны реализовывать функции, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="4acd6-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="4acd6-106">Возвращаемая величина, упомянутая в справочных разделах в этом разделе, определена в SDK include file, xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="4acd6-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="4acd6-107">Архитектура соединители кластера</span><span class="sxs-lookup"><span data-stu-id="4acd6-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="4acd6-108">Excel вызывает точки входа в соединитель кластера для передачи вызовов пользовательских функций в высокоскоростной вычислительный кластер и для управления сеансами кластера.</span><span class="sxs-lookup"><span data-stu-id="4acd6-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="4acd6-109">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="4acd6-109">In this section</span></span>

[<span data-ttu-id="4acd6-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="4acd6-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="4acd6-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="4acd6-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="4acd6-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="4acd6-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="4acd6-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="4acd6-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="4acd6-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="4acd6-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="4acd6-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="4acd6-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="4acd6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4acd6-116">See also</span></span>



[<span data-ttu-id="4acd6-117">Разработка соединителей кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="4acd6-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="4acd6-118">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="4acd6-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)


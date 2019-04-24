---
title: Функции соединителя кластера Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311069"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="1159b-103">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="1159b-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="1159b-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1159b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1159b-105">В библиотеках DLL соединителя кластера Microsoft Excel 2013 должны быть реализованы функции, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1159b-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="1159b-106">Возвращаемые значения, указанные в разделах справочника в этом разделе, определены в файле SDK include, Xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="1159b-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="1159b-107">Архитектура соединителя кластера</span><span class="sxs-lookup"><span data-stu-id="1159b-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="1159b-108">Excel вызывает точки входа в кластерном соединителе для передачи вызовов пользовательских функций в высокопроизводительный вычислительный кластер, а для управления сеансом кластера.</span><span class="sxs-lookup"><span data-stu-id="1159b-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1159b-109">Содержание</span><span class="sxs-lookup"><span data-stu-id="1159b-109">In this section</span></span>

[<span data-ttu-id="1159b-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="1159b-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="1159b-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="1159b-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="1159b-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="1159b-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="1159b-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="1159b-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="1159b-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="1159b-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="1159b-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="1159b-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="1159b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1159b-116">See also</span></span>



[<span data-ttu-id="1159b-117">Разработка соединителей кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="1159b-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="1159b-118">Функции защиты кластеров</span><span class="sxs-lookup"><span data-stu-id="1159b-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)


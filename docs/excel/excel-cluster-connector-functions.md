---
title: Функции соединителя кластера Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807177"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="d54d5-103">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="d54d5-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="d54d5-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d54d5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d54d5-105">Соединитель кластера Microsoft Excel 2013 библиотеки DLL необходимо реализовать функции, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d54d5-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="d54d5-106">Возвращаемые значения, упомянутые в ссылки в этом разделе определяются в пакете SDK включают файл, xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="d54d5-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="d54d5-107">Архитектура соединителя кластера</span><span class="sxs-lookup"><span data-stu-id="d54d5-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="d54d5-108">Excel вызывает точки входа в соединитель кластера передача пользовательской функции вызова к высокой производительности вычислительному кластеру, а также для управления сеансами кластера.</span><span class="sxs-lookup"><span data-stu-id="d54d5-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d54d5-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d54d5-109">In this section</span></span>

[<span data-ttu-id="d54d5-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="d54d5-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="d54d5-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="d54d5-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="d54d5-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="d54d5-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="d54d5-113">Метод OpenSession</span><span class="sxs-lookup"><span data-stu-id="d54d5-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="d54d5-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="d54d5-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="d54d5-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="d54d5-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="d54d5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d54d5-116">See also</span></span>



[<span data-ttu-id="d54d5-117">���������� ������������ ��������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="d54d5-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="d54d5-118">Безопасные для кластера функции</span><span class="sxs-lookup"><span data-stu-id="d54d5-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)


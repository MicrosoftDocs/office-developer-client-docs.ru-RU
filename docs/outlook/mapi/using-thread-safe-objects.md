---
title: Использование Thread-Safe объектов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425171"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="68371-103">Использование Thread-Safe объектов</span><span class="sxs-lookup"><span data-stu-id="68371-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="68371-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68371-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68371-105">Клиентские приложения могут предположить, что объекты, используемые напрямую или в качестве откатов, всегда безопасны для потоков, за исключением следующих случаев:</span><span class="sxs-lookup"><span data-stu-id="68371-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="68371-106">Объект состояния поставщика транспорта, полученный в результате клиентского вызова [в IMAPISession::OpenEntry](imapisession-openentry.md) с идентификатором входа из строки таблицы состояния поставщика.</span><span class="sxs-lookup"><span data-stu-id="68371-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="68371-107">Все объекты формы MAPI, полученные с помощью клиентского вызова [в MAPIOpenFormMgr.](mapiopenformmgr.md)</span><span class="sxs-lookup"><span data-stu-id="68371-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="68371-108">Объекты форм подчиняются правилам модели квартиры, и клиенты должны использовать их и все объекты, содержащиеся в них, только в созданном ими потоке.</span><span class="sxs-lookup"><span data-stu-id="68371-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="68371-109">Когда клиент получает доступ к строке поставщика транспорта в таблице состояния, которая включает идентификатор входа связанного объекта состояния, клиент может вызвать **OpenEntry** с этим идентификатором входа, чтобы открыть объект состояния.</span><span class="sxs-lookup"><span data-stu-id="68371-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="68371-110">Этот объект состояния не является безопасным для потоков, так как поставщики транспорта работают в контексте пулера MAPI и не поддерживают отдельный контекст для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="68371-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="68371-111">Объект состояния подчиняется правилам модели квартиры, и клиенты должны использовать его только в созданном потоке.</span><span class="sxs-lookup"><span data-stu-id="68371-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="68371-112">Клиент также должен вызывать [MAPIInitialize](mapiinitialize.md) на каждом потоке, прежде чем использовать любые объекты MAPI и [MAPIUninitialize,](mapiuninitialize.md) когда это использование будет завершено.</span><span class="sxs-lookup"><span data-stu-id="68371-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="68371-113">Эти вызовы должны быть сделаны, даже если используемые объекты передаются потоку из внешнего источника.</span><span class="sxs-lookup"><span data-stu-id="68371-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="68371-114">**MAPIInitialize** и **MAPIUninitialize** можно вызывать из любого места, за исключением функции Win32 **DllMain,** функции, вызываемой системой при инициализации и прекращении процессов и потоков, или при вызовах функций **LoadLibrary** и **FreeLibrary.**</span><span class="sxs-lookup"><span data-stu-id="68371-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="68371-115">Объекты косвенного использования никогда не должны считаться безопасными для потоков.</span><span class="sxs-lookup"><span data-stu-id="68371-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="68371-116">Объекты косвенного использования возвращаются методами, которые требуют указателей интерфейса назначения в качестве параметров ввода.</span><span class="sxs-lookup"><span data-stu-id="68371-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="68371-117">Примерами таких методов являются **IMAPIProp::CopyTo** и **CopyProps,** **IMAPIFolder::CopyFolder** и **CopyMessage** и **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="68371-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="68371-118">Если поставщик службы хочет вызвать такой объект из потока, за исключением того, на котором он был передан, поставщик несет ответственность за явное маршалинг объекта.</span><span class="sxs-lookup"><span data-stu-id="68371-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  


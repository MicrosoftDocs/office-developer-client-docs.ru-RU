---
title: Использование потокобезопасных объектов
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
# <a name="using-thread-safe-objects"></a><span data-ttu-id="81ba3-103">Использование потокобезопасных объектов</span><span class="sxs-lookup"><span data-stu-id="81ba3-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="81ba3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ba3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ba3-105">Клиентские приложения могут предполагать, что объекты, которые использовались напрямую или как обратные вызовы, всегда являются потокобезопасными, за исключением следующих случаев:</span><span class="sxs-lookup"><span data-stu-id="81ba3-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="81ba3-106">Объект состояния поставщика транспорта, полученный через клиентский вызов [IMAPISession:: OpenEntry](imapisession-openentry.md) с идентификатором записи из строки таблицы состояния поставщика.</span><span class="sxs-lookup"><span data-stu-id="81ba3-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="81ba3-107">Все объекты форм MAPI, полученные с помощью клиентского вызова в [мапиопенформмгр](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="81ba3-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="81ba3-108">Объекты форм следует использовать для правил и клиентов апартаментной модели, а также все объекты, которые они содержат, только в создавшем их потоке.</span><span class="sxs-lookup"><span data-stu-id="81ba3-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="81ba3-109">Когда клиент получает доступ к строке поставщика транспорта в таблице status, включающей идентификатор связанного объекта status, клиент может вызвать **OpenEntry** с этим идентификатором записи, чтобы открыть объект Status.</span><span class="sxs-lookup"><span data-stu-id="81ba3-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="81ba3-110">Этот объект Status не является потокобезопасным, так как поставщики транспорта работают в контексте диспетчера очереди MAPI и не сохраняют отдельный контекст для своего объекта Status.</span><span class="sxs-lookup"><span data-stu-id="81ba3-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="81ba3-111">Объект Status подчиняется правилам, связанным с апартаментной моделью, и клиенты должны использовать его только в создавшем его потоке.</span><span class="sxs-lookup"><span data-stu-id="81ba3-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="81ba3-112">Кроме того, клиент должен вызвать [мапиинитиализе](mapiinitialize.md) для каждого потока перед использованием любых объектов MAPI и [мапиунинитиализе](mapiuninitialize.md) при завершении использования.</span><span class="sxs-lookup"><span data-stu-id="81ba3-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="81ba3-113">Эти вызовы должны быть сделаны, даже если используемые объекты передаются в поток из внешнего источника.</span><span class="sxs-lookup"><span data-stu-id="81ba3-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="81ba3-114">**Мапиинитиализе** и **мапиунинитиализе** можно вызывать из любого места за исключением того, что в функции Win32 **DllMain** функция, вызываемая системой при инициализации и завершении процессов и потоков, а также при вызовах \*\* Функции LoadLibrary\*\* и **FreeLibrary** .</span><span class="sxs-lookup"><span data-stu-id="81ba3-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="81ba3-115">Никогда не следует предполагать, что объекты косвенного использования не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="81ba3-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="81ba3-116">Объекты косвенного использования возвращаются методами, которые потребуют указателей конечного интерфейса в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="81ba3-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="81ba3-117">Примеры таких методов **: IMAPIProp:: CopyTo** и **копипропс**, **IMAPIFolder:: CopyFolder** и **копимессаже**и **имсгсервицеадмин:: копимсгсервице**.</span><span class="sxs-lookup"><span data-stu-id="81ba3-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="81ba3-118">Если поставщик услуг хочет вызвать такой объект из потока, отличного от того, в котором он был передан, поставщик несет ответственность за явное маршалирование объекта.</span><span class="sxs-lookup"><span data-stu-id="81ba3-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  


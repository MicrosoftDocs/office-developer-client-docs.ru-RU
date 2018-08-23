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
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580980"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="6caec-103">Использование потокобезопасных объектов</span><span class="sxs-lookup"><span data-stu-id="6caec-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="6caec-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6caec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6caec-105">Клиентские приложения можно допустить, что объекты непосредственно или как обратные вызовы всегда являются потокобезопасными за исключением в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="6caec-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="6caec-106">Объект состояния поставщика транспорта получить с помощью клиента вызов [IMAPISession::OpenEntry](imapisession-openentry.md) с идентификатором записи из строки состояния таблицы поставщика.</span><span class="sxs-lookup"><span data-stu-id="6caec-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="6caec-107">Получить с помощью вызова клиента [MAPIOpenFormMgr](mapiopenformmgr.md)все объекты формы MAPI.</span><span class="sxs-lookup"><span data-stu-id="6caec-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="6caec-108">Объекты формы соблюдать правила модели подразделения и клиенты должны использовать их и все объекты, содержащиеся в них только в потоке, создавшего их.</span><span class="sxs-lookup"><span data-stu-id="6caec-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="6caec-109">При обращении поставщика транспорта строки в таблице состояния, которая включает в себя идентификатор записи объекта связанного состояния, клиент может вызывать **OpenEntry** с этим идентификатором записи для открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="6caec-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="6caec-110">Этот объект состояния не являющихся потокобезопасными, так как поставщики транспорта выполняться в контексте диспетчер очереди MAPI и не поддерживать отдельные контекста для их состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6caec-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="6caec-111">Состояние объекта подчиняется правилам модели подразделения и клиенты должны использовать только в потоке, который он был создан.</span><span class="sxs-lookup"><span data-stu-id="6caec-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="6caec-112">Перед использованием любых объектов MAPI и [MAPIUninitialize](mapiuninitialize.md) после завершения, в которых используется клиентом необходимо вызвать в на каждый поток [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="6caec-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="6caec-113">Эти вызовы следует выполнить даже в том случае, если объекты для использования в систему, передаются в поток из внешнего источника.</span><span class="sxs-lookup"><span data-stu-id="6caec-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="6caec-114">**MAPIInitialize** и **MAPIUninitialize** могут вызываться из в любом месте за исключением из в функцию Win32 **DllMain** , функция, которая вызывается системой при процессы и потоки инициализируется и завершен или при вызовы ** LoadLibrary** и функции **FreeLibrary** .</span><span class="sxs-lookup"><span data-stu-id="6caec-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="6caec-115">Косвенные использовать объекты должны никогда не оценивается в являющихся потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="6caec-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="6caec-116">Косвенные использования объектов, методов, которые требуют указателей интерфейса назначения в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="6caec-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="6caec-117">Примеры таких методов, **IMAPIProp::CopyTo** и **CopyProps**, **IMAPIFolder::CopyFolder** и **CopyMessage**и **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="6caec-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="6caec-118">Если поставщик услуг хочет вызов такой объект из потока, отличного от того, для которого был передан, поставщик несет ответственность за явно маршалинга объекта.</span><span class="sxs-lookup"><span data-stu-id="6caec-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  


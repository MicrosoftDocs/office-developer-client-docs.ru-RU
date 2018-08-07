---
title: Запуск формы для чтения сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809649"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="4650e-103">Запуск формы для чтения сообщения</span><span class="sxs-lookup"><span data-stu-id="4650e-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="4650e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4650e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4650e-105">Специалистов по внедрению сервера форм следует ожидать следующую последовательность вызовов их server формы и объекты формы при загрузке клиентского приложения сообщение:</span><span class="sxs-lookup"><span data-stu-id="4650e-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="4650e-106">Клиентское приложение Откроется диспетчер форм с вызова функции [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="4650e-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="4650e-107">Клиентское приложение вызывает метод [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , который возвращает объект с [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="4650e-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="4650e-108">Диспетчер форм может выпущен теперь, если он не будет использоваться для дальнейшей активаций формы.</span><span class="sxs-lookup"><span data-stu-id="4650e-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="4650e-109">Обратите внимание, что вызов **LoadForm** может занять некоторое время, так как может потребоваться установка исполняемых файлов сервера формы перед тем как диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="4650e-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="4650e-110">При необходимости в клиентском приложении можно подготовить [IMAPIViewContext](imapiviewcontextiunknown.md) операциям элемента управления, которые могут привести объект формы для загрузки предыдущему или следующему сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="4650e-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="4650e-111">В клиентском приложении можно использовать метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) для изменения контекста представления по умолчанию, которое было задано в вызове **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="4650e-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="4650e-112">Клиентское приложение вызывает метод [IPersistMessage::Load](ipersistmessage-load.md) для загрузки данных сообщений в объект формы.</span><span class="sxs-lookup"><span data-stu-id="4650e-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="4650e-113">Клиентское приложение вызывает [IMAPIForm::DoVerb](imapiform-doverb.md) для вызова open команды, передав дополнительный указатель интерфейса [IMAPIViewContext](imapiviewcontextiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4650e-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4650e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4650e-114">See also</span></span>



[<span data-ttu-id="4650e-115">Взаимодействие серверов форм</span><span class="sxs-lookup"><span data-stu-id="4650e-115">Form Server Interactions</span></span>](form-server-interactions.md)


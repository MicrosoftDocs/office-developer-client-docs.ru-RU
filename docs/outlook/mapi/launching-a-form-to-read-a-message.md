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
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425934"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="52d42-103">Запуск формы для чтения сообщения</span><span class="sxs-lookup"><span data-stu-id="52d42-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="52d42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52d42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52d42-105">Реализутелям серверов форм следует ожидать следующей последовательности вызовов метода на сервер формы и объекты формы при загрузке клиентского приложения сообщения:</span><span class="sxs-lookup"><span data-stu-id="52d42-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="52d42-106">Клиентская заявка открывает диспетчер форм с вызовом на функцию [MAPIOpenFormMgr.](mapiopenformmgr.md)</span><span class="sxs-lookup"><span data-stu-id="52d42-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="52d42-107">Клиентская заявка вызывает [метод IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) который возвращает объект [с помощью IMAPIForm.](imapiformiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="52d42-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="52d42-108">Менеджер формы может быть выпущен сейчас, если он не будет использоваться для дальнейших активаций формы.</span><span class="sxs-lookup"><span data-stu-id="52d42-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="52d42-109">Обратите внимание, что вызов **в LoadForm может** занять некоторое время, так как диспетчеру форм может потребоваться установить исполняемые файлы сервера форм перед началом выполнения.</span><span class="sxs-lookup"><span data-stu-id="52d42-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="52d42-110">Дополнительно клиентская заявка может подготовить [IMAPIViewContext](imapiviewcontextiunknown.md) для управления операциями, которые могут привести к загрузке объекта формы предыдущего или следующего сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="52d42-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="52d42-111">Клиентская заявка может использовать [метод IMAPIForm::SetViewContext](imapiform-setviewcontext.md) для изменения контекста представления по умолчанию, установленного в **вызове LoadForm.**</span><span class="sxs-lookup"><span data-stu-id="52d42-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="52d42-112">Клиентская заявка вызывает [метод IPersistMessage::Load](ipersistmessage-load.md) для загрузки данных сообщений в объект формы.</span><span class="sxs-lookup"><span data-stu-id="52d42-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="52d42-113">Клиентская заявка вызывает [IMAPIForm::D oVerb,](imapiform-doverb.md) чтобы вызвать открытый глагол, передав необязательный указатель [интерфейса IMAPIViewContext.](imapiviewcontextiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="52d42-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="52d42-114">См. также</span><span class="sxs-lookup"><span data-stu-id="52d42-114">See also</span></span>



[<span data-ttu-id="52d42-115">Взаимодействие с сервером форм</span><span class="sxs-lookup"><span data-stu-id="52d42-115">Form Server Interactions</span></span>](form-server-interactions.md)


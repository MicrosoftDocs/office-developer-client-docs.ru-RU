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
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="99146-103">Запуск формы для чтения сообщения</span><span class="sxs-lookup"><span data-stu-id="99146-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="99146-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99146-105">Разработчикам, реализующим сервер форм, следует ожидать приведенной ниже последовательности вызовов методов к их серверу форм и объектам формы, когда клиентское приложение загружает сообщение:</span><span class="sxs-lookup"><span data-stu-id="99146-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="99146-106">Клиентское приложение открывает Диспетчер форм с вызовом функции [мапиопенформмгр](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="99146-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="99146-107">Клиентское приложение вызывает метод [имапиформмгр:: лоадформ](imapiformmgr-loadform.md) , который возвращает объект с [имапиформ](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="99146-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="99146-108">Диспетчер форм может быть выпущен в данный момент, если он не будет использоваться для дальнейших активаций форм.</span><span class="sxs-lookup"><span data-stu-id="99146-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="99146-109">Обратите внимание, что при вызове **лоадформ** может потребоваться некоторое время, так как диспетчеру форм может потребоваться установить исполняемые файлы сервера форм, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="99146-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="99146-110">Кроме того, клиентское приложение может подготовить [имапивиевконтекст](imapiviewcontextiunknown.md) к операциям управления, которые могут привести к тому, что объект формы загрузит предыдущее или следующее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="99146-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="99146-111">Клиентское приложение может использовать метод [имапиформ:: сетвиевконтекст](imapiform-setviewcontext.md) , чтобы изменить контекст представления по умолчанию, заданный в вызове **лоадформ** .</span><span class="sxs-lookup"><span data-stu-id="99146-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="99146-112">Клиентское приложение вызывает метод [иперсистмессаже:: Load](ipersistmessage-load.md) для загрузки данных сообщения в объект Form.</span><span class="sxs-lookup"><span data-stu-id="99146-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="99146-113">Клиентское приложение вызывает [имапиформ::D оверб](imapiform-doverb.md) для вызова команды Open, передавая Необязательный указатель интерфейса [имапивиевконтекст](imapiviewcontextiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="99146-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="99146-114">См. также</span><span class="sxs-lookup"><span data-stu-id="99146-114">See also</span></span>



[<span data-ttu-id="99146-115">Взаимодействие с сервером форм</span><span class="sxs-lookup"><span data-stu-id="99146-115">Form Server Interactions</span></span>](form-server-interactions.md)


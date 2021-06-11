---
title: Объекты формы MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404787"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="84d81-103">Объекты формы MAPI</span><span class="sxs-lookup"><span data-stu-id="84d81-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="84d81-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84d81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84d81-105">Объекты form создаются динамически с помощью серверов форм, чтобы отображать определенные сообщения и позволять пользователям взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="84d81-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="84d81-106">Таким образом, объект формы — это мгновенный вывод класса из [IMAPIForm,](imapiformiunknown.md) реализуемого сервером форм.</span><span class="sxs-lookup"><span data-stu-id="84d81-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="84d81-107">Когда клиентская заявка открывает сообщение, сервер формы для этого класса сообщений создает объект формы для обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="84d81-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="84d81-108">Объект формы создает интерфейс и отображает свойства сообщения в нем.</span><span class="sxs-lookup"><span data-stu-id="84d81-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="84d81-109">Объект формы и его интерфейс сохраняются до тех пор, пока пользователь не закроет его.</span><span class="sxs-lookup"><span data-stu-id="84d81-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="84d81-110">Объект формы обрабатывает любые изменения значений свойств сообщения.</span><span class="sxs-lookup"><span data-stu-id="84d81-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="84d81-111">Кроме того, интерфейсы форм MAPI определяют механизм, с помощью которого один объект формы может загружать и отображать ряд сообщений.</span><span class="sxs-lookup"><span data-stu-id="84d81-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="84d81-112">Это механизм эффективности, который позволяет избежать необходимости уничтожения и создания объектов сообщений и их интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="84d81-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="84d81-113">Если клиент обмена сообщениями запрашивает загрузку другого сообщения, объект формы должен сохранить все изменения в свойствах текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="84d81-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="84d81-114">Сведения о перспективах объектов форм в клиентском приложении см. в приложении [MAPI Custom Form Objects.](mapi-custom-form-objects.md)</span><span class="sxs-lookup"><span data-stu-id="84d81-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84d81-115">См. также</span><span class="sxs-lookup"><span data-stu-id="84d81-115">See also</span></span>



[<span data-ttu-id="84d81-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="84d81-116">MAPI Forms</span></span>](mapi-forms.md)


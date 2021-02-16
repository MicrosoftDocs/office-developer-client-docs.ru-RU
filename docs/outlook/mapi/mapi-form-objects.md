---
title: Объекты форм MAPI
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
# <a name="mapi-form-objects"></a><span data-ttu-id="cae30-103">Объекты форм MAPI</span><span class="sxs-lookup"><span data-stu-id="cae30-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="cae30-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae30-105">Объекты форм динамически создаются серверами форм для отображения определенных сообщений и обеспечения взаимодействия пользователей с ними.</span><span class="sxs-lookup"><span data-stu-id="cae30-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="cae30-106">Таким образом, объект формы является копией класса, производного от [IMAPIForm,](imapiformiunknown.md) который реализуется сервером форм.</span><span class="sxs-lookup"><span data-stu-id="cae30-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="cae30-107">Когда клиентская приложение открывает сообщение, сервер форм для этого класса сообщений создает объект формы для обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="cae30-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="cae30-108">Затем объект формы создает свой интерфейс и отображает свойства сообщения в нем.</span><span class="sxs-lookup"><span data-stu-id="cae30-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="cae30-109">Объект формы и его интерфейс сохраняются, пока пользователь не закроет его.</span><span class="sxs-lookup"><span data-stu-id="cae30-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="cae30-110">Объект формы обрабатывает любые изменения значений свойств сообщения.</span><span class="sxs-lookup"><span data-stu-id="cae30-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="cae30-111">Кроме того, интерфейсы форм MAPI определяют механизм, с помощью которого один объект формы может загружать и отображать серию сообщений.</span><span class="sxs-lookup"><span data-stu-id="cae30-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="cae30-112">Это механизм эффективности, который позволяет избежать необходимости уничтожения и создания объектов сообщений и их интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="cae30-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="cae30-113">Когда клиент обмена сообщениями запрашивает загрузку другого сообщения, объект формы должен сохранить все изменения в свойствах текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="cae30-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="cae30-114">Сведения о перспективе объектов форм в клиентском приложении см. в поддоме "Объекты [настраиваемой формы MAPI".](mapi-custom-form-objects.md)</span><span class="sxs-lookup"><span data-stu-id="cae30-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cae30-115">См. также</span><span class="sxs-lookup"><span data-stu-id="cae30-115">See also</span></span>



[<span data-ttu-id="cae30-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="cae30-116">MAPI Forms</span></span>](mapi-forms.md)


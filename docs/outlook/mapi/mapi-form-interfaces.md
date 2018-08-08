---
title: Интерфейсы форм MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8452a6e49059dd0912f1efffef7e749afd6cdf6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809735"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="2048e-103">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="2048e-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="2048e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2048e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2048e-105">MAPI определяет следующие интерфейсы, связанные с форм.</span><span class="sxs-lookup"><span data-stu-id="2048e-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="2048e-106">**Имя интерфейса**</span><span class="sxs-lookup"><span data-stu-id="2048e-106">**Interface name**</span></span>|<span data-ttu-id="2048e-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2048e-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2048e-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="2048e-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="2048e-109">Управляет объектам формы и обработка команд объекта формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="2048e-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2048e-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="2048e-111">Определяет может обрабатывать следующего сообщения и изменяет состояние следующий или предыдущий объект формы, объекта формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="2048e-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="2048e-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="2048e-113">Поддерживает установку, deinstallation и разрешение серверов формы с контейнером конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="2048e-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="2048e-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="2048e-115">Поддерживает использование серверов настраиваемые формы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2048e-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="2048e-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="2048e-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="2048e-117">Позволяет клиентским приложениям для работы со свойствами, которые специфичны для класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="2048e-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="2048e-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="2048e-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="2048e-119">Позволяет клиентским приложениям для получения сведений о форме серверы, активирует серверы формы и устанавливает серверы формы в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2048e-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="2048e-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="2048e-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="2048e-121">Используется для работы с сообщений, связанных с объектами формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="2048e-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2048e-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="2048e-123">Уведомляет клиентские приложения, которые в объекте формы возникновении события.</span><span class="sxs-lookup"><span data-stu-id="2048e-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="2048e-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="2048e-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="2048e-125">Использовать реагировать на Далее, назад и удаление команд в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="2048e-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="2048e-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="2048e-127">Служит для сохранения, инициализации и загрузки объектов формы между хранение сообщений.</span><span class="sxs-lookup"><span data-stu-id="2048e-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="2048e-128">Дополнительные сведения о методах интерфейсы формы MAPI документации для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2048e-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="2048e-129">Необходимо реализовать все интерфейсы формы MAPI для создания настраиваемых форм.</span><span class="sxs-lookup"><span data-stu-id="2048e-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="2048e-130">Форма самого требует только реализовать **IPersistMessage**, **IMAPIForm**и **IMAPIFormAdviseSink** интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2048e-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="2048e-131">Кроме того рекомендуется также реализовать **IMAPIFormFactory** и **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="2048e-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="2048e-132">**IMAPIFormFactory** полезен для соответствия требованиям OLE и **IMAPIFormInfo** позволяет хорошо написанных клиентских приложений лучше использовать формы.</span><span class="sxs-lookup"><span data-stu-id="2048e-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2048e-133">Строго сферой **IMAPIFormAdviseSink** — это необязательный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2048e-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="2048e-134">Тем не менее настоятельно рекомендуется реализовать в форме серверы.</span><span class="sxs-lookup"><span data-stu-id="2048e-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="2048e-135">Этот интерфейс важно эффективное взаимодействие между обмена сообщениями клиентов и серверов форм, особенно если несколько сообщений сервера форм класс сообщения обрабатывают.</span><span class="sxs-lookup"><span data-stu-id="2048e-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2048e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2048e-136">See also</span></span>



[<span data-ttu-id="2048e-137">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="2048e-137">MAPI Forms</span></span>](mapi-forms.md)


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
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412347"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="7f735-103">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="7f735-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="7f735-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f735-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f735-105">MAPI определяет следующие интерфейсы, связанные с формами.</span><span class="sxs-lookup"><span data-stu-id="7f735-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="7f735-106">**Имя интерфейса**</span><span class="sxs-lookup"><span data-stu-id="7f735-106">**Interface name**</span></span>|<span data-ttu-id="7f735-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f735-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f735-108">Имапиформ</span><span class="sxs-lookup"><span data-stu-id="7f735-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="7f735-109">Управляет объектами формы и обрабатывает команды объекта формы.</span><span class="sxs-lookup"><span data-stu-id="7f735-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="7f735-110">Имапиформадвисесинк</span><span class="sxs-lookup"><span data-stu-id="7f735-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="7f735-111">Определяет, может ли объект Form обработать следующее сообщение и изменить следующее или предыдущее состояние объекта Form.</span><span class="sxs-lookup"><span data-stu-id="7f735-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f735-112">Имапиформконтаинер</span><span class="sxs-lookup"><span data-stu-id="7f735-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="7f735-113">Поддерживает установку, удаление и решение серверов форм с определенным контейнером форм.</span><span class="sxs-lookup"><span data-stu-id="7f735-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="7f735-114">Имапиформфактори</span><span class="sxs-lookup"><span data-stu-id="7f735-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="7f735-115">Поддерживает использование настраиваемых серверов форм времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f735-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="7f735-116">Имапиформинфо</span><span class="sxs-lookup"><span data-stu-id="7f735-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="7f735-117">Позволяет клиентским приложениям работать со свойствами, характерными для класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f735-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="7f735-118">Имапиформмгр</span><span class="sxs-lookup"><span data-stu-id="7f735-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="7f735-119">Позволяет клиентским приложениям получать сведения о серверах форм, активировать серверы форм и устанавливать серверы форм в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7f735-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="7f735-120">Имапимессажесите</span><span class="sxs-lookup"><span data-stu-id="7f735-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="7f735-121">Используется для управления сообщениями, связанными с объектами формы.</span><span class="sxs-lookup"><span data-stu-id="7f735-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="7f735-122">Имапивиевадвисесинк</span><span class="sxs-lookup"><span data-stu-id="7f735-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="7f735-123">Уведомляет клиентские приложения о том, что в объекте формы возникло событие.</span><span class="sxs-lookup"><span data-stu-id="7f735-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f735-124">Имапивиевконтекст</span><span class="sxs-lookup"><span data-stu-id="7f735-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="7f735-125">Используется для ответа на команды "Далее", "назад" и "Удалить" в объекте Form.</span><span class="sxs-lookup"><span data-stu-id="7f735-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f735-126">Иперсистмессаже</span><span class="sxs-lookup"><span data-stu-id="7f735-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="7f735-127">Используется для сохранения, инициализации и загрузки объектов формы в хранилище сообщений и из него.</span><span class="sxs-lookup"><span data-stu-id="7f735-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="7f735-128">Для получения дополнительных сведений о методах интерфейсов форм MAPI ознакомьтесь с документацией по этим интерфейсам.</span><span class="sxs-lookup"><span data-stu-id="7f735-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="7f735-129">Для создания настраиваемой формы не требуется реализовывать все интерфейсы форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f735-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="7f735-130">Для формы необходимо, чтобы были реализованы только интерфейсы **иперсистмессаже**, **имапиформ**и **имапиформадвисесинк** .</span><span class="sxs-lookup"><span data-stu-id="7f735-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="7f735-131">Кроме того, рекомендуется реализовать **имапиформфактори** и **имапиформинфо**.</span><span class="sxs-lookup"><span data-stu-id="7f735-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="7f735-132">**Имапиформфактори** полезен для обеспечения соответствия требованиям OLE, и **имапиформинфо** позволяет использовать хорошо написанные клиентские приложения, чтобы лучше использовать формы.</span><span class="sxs-lookup"><span data-stu-id="7f735-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f735-133">Строго говоря, **имапиформадвисесинк** — необязательный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7f735-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="7f735-134">Тем не менее, настоятельно рекомендуется реализовать его на серверах форм.</span><span class="sxs-lookup"><span data-stu-id="7f735-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="7f735-135">Этот интерфейс очень важен для эффективного взаимодействия между клиентами обмена сообщениями и серверами форм, особенно при использовании нескольких сообщений класса сообщений сервера форм.</span><span class="sxs-lookup"><span data-stu-id="7f735-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f735-136">См. также</span><span class="sxs-lookup"><span data-stu-id="7f735-136">See also</span></span>



[<span data-ttu-id="7f735-137">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="7f735-137">MAPI Forms</span></span>](mapi-forms.md)


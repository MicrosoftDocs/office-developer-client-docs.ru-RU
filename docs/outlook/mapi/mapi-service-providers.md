---
title: Поставщиков служб MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3f1cab24ef6bbd632ee3dc204e93f59e6f9ac846
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809843"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="47953-103">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="47953-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="47953-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47953-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47953-105">Существует три общие типы поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="47953-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="47953-106">Адресной книги поставщиков.</span><span class="sxs-lookup"><span data-stu-id="47953-106">Address book providers.</span></span>
    
- <span data-ttu-id="47953-107">Поставщики хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="47953-107">Message store providers.</span></span>
    
- <span data-ttu-id="47953-108">Поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="47953-108">Transport providers.</span></span>
    
<span data-ttu-id="47953-109">Поставщиков хранилища адресной книги и сообщение имеет много общего.</span><span class="sxs-lookup"><span data-stu-id="47953-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="47953-110">Они зарегистрируйте уникальный идентификатор MAPI, используемых для создания идентификаторы записей для объектов.</span><span class="sxs-lookup"><span data-stu-id="47953-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="47953-111">Они предоставляют иерархия объектов и свойств, которые клиенты могут получить доступ к и работа с элементами управления.</span><span class="sxs-lookup"><span data-stu-id="47953-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="47953-112">Для объектов контейнера они поддерживают иерархии таблица и таблица содержимое.</span><span class="sxs-lookup"><span data-stu-id="47953-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="47953-113">Они поддерживают уведомления о событии на эти таблицы и при необходимости для отдельных объектов, чтобы клиенты могут получать сведения об изменениях, произошедшие во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="47953-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="47953-114">При длительных операций, которые могут быть отображены индикатор выполнения для оповещения пользователя о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="47953-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="47953-115">Клиенты могут взаимодействовать с поставщиками хранилища адресной книги и сообщения либо косвенно через MAPI с помощью [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) и [IMAPISession: IUnknown](imapisessioniunknown.md) интерфейсы или непосредственно с помощью одного из интерфейсов поставщика службы в в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="47953-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="47953-116">**Адресной книги поставщика интерфейсов**</span><span class="sxs-lookup"><span data-stu-id="47953-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="47953-117">**Интерфейсы поставщика хранилища сообщений**</span><span class="sxs-lookup"><span data-stu-id="47953-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47953-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="47953-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="47953-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47953-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="47953-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="47953-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="47953-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="47953-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="47953-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47953-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="47953-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47953-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="47953-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47953-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="47953-125">Поставщики транспорта отличаются от адресной книги и сообщения поставщиков хранилища, как они обмениваться данными MAPI и с клиентами.</span><span class="sxs-lookup"><span data-stu-id="47953-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="47953-126">Поставщики транспорта обычно дождитесь MAPI запрашивать сведения, а не связь.</span><span class="sxs-lookup"><span data-stu-id="47953-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="47953-127">В отличие от других поставщиков поставщиками транспорта не поддерживают различные объекты и таблиц, используемых клиентами.</span><span class="sxs-lookup"><span data-stu-id="47953-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="47953-128">Тем не менее они поддерживают состояние объекта, как сделать всех поставщиков услуг и опубликовать его свойства в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="47953-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="47953-129">В то время как поставщиков хранилища адресной книги и сообщения вызвать метод [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникальных идентификаторов для создания их идентификаторы записей, поставщиками транспорта вызовите метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для Регистрация уникальных идентификаторов, а также типы адресов для о доставки определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="47953-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="47953-130">Поставщик услуг должен иметь три файлы заголовков: один файл общедоступных заголовка и два внутренних файлов.</span><span class="sxs-lookup"><span data-stu-id="47953-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="47953-131">Используйте файл общедоступных заголовка для конфигурации и документирования свойства и их значения.</span><span class="sxs-lookup"><span data-stu-id="47953-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="47953-132">Включить в один из файлов внутреннего заголовка всех необходимых общедоступных MAPI заголовков; файл заголовка должно быть включено во всех исходных файлов поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="47953-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="47953-133">Использование внутренних файлов для определения кодов ресурса.</span><span class="sxs-lookup"><span data-stu-id="47953-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="47953-134">Адресная книга, хранилища сообщений и поставщиками транспорта выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="47953-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="47953-135">Передать функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="47953-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="47953-136">Укажите поставщика и вход в систему для обработки входа в систему и инициализации.</span><span class="sxs-lookup"><span data-stu-id="47953-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="47953-137">Если принадлежит поставщик службы сообщений укажите функцию точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="47953-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="47953-138">Поддержка настройки при помощи свойств.</span><span class="sxs-lookup"><span data-stu-id="47953-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="47953-139">Состояние объекта и обеспечивающие ее использование в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="47953-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="47953-140">Дескриптор, завершение работы.</span><span class="sxs-lookup"><span data-stu-id="47953-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47953-141">См. также</span><span class="sxs-lookup"><span data-stu-id="47953-141">See also</span></span>



[<span data-ttu-id="47953-142">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="47953-142">MAPI Concepts</span></span>](mapi-concepts.md)


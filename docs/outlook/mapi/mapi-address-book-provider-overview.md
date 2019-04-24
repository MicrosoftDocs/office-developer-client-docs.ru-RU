---
title: Общие сведения о поставщике адресной книги MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298146"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="34e08-103">Общие сведения о поставщике адресной книги MAPI</span><span class="sxs-lookup"><span data-stu-id="34e08-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="34e08-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34e08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34e08-105">Поставщики адресных книг обрабатывают доступ к данным каталога.</span><span class="sxs-lookup"><span data-stu-id="34e08-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="34e08-106">Сведения о каталоге состоят из данных для двух типов получателей сообщений: индивидуальные пользователи и группы пользователей обмена сообщениями, которые обычно задаются совместно в списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="34e08-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="34e08-107">В зависимости от типа получателя и поставщика адресных книг можно сделать доступным широкий спектр данных.</span><span class="sxs-lookup"><span data-stu-id="34e08-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="34e08-108">Например, все поставщики адресных книг хранят имя, адрес и тип адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="34e08-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="34e08-109">Каждый поставщик адресных книг организует эти данные с помощью одного или нескольких контейнеров.</span><span class="sxs-lookup"><span data-stu-id="34e08-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="34e08-110">Число и структура контейнеров зависят от реализации поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="34e08-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="34e08-111">Например, один поставщик адресной книги может использовать один контейнер для хранения всей информации, другой может использовать один контейнер верхнего уровня, который содержит подконтейнеры, а третья — несколько контейнеров верхнего уровня, каждый из которых содержит подконтейнеры.</span><span class="sxs-lookup"><span data-stu-id="34e08-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="34e08-112">Иерархия контейнеров адресных книг может быть достаточно глубокой; количество подконтейнеров, которые можно использовать, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="34e08-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="34e08-113">На следующем рисунке показана типичная организация адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="34e08-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="34e08-114">**Организация адресной книги**</span><span class="sxs-lookup"><span data-stu-id="34e08-114">**Address book organization**</span></span>
  
<span data-ttu-id="34e08-115">![Организация адресной книги] (media/amapi_04.gif "Организация адресной книги")</span><span class="sxs-lookup"><span data-stu-id="34e08-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="34e08-116">MAPI интегрирует всю информацию, предоставленную установленными поставщиками адресных книг, в одну адресную книгу, представляя единое представление для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="34e08-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="34e08-117">В интегрированном списке показаны контейнеры верхнего уровня, отображаемые каждым из установленных поставщиков адресной книги.</span><span class="sxs-lookup"><span data-stu-id="34e08-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="34e08-118">Большинство поставщиков адресных книг предоставляют только несколько контейнеров (обычно от одного до трех) на верхнем уровне для включения в верхний уровень встроенной адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="34e08-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="34e08-119">Например, поставщик адресных книг может сделать доступными "все пользователи" и "Локальные пользователи" как два контейнера на верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="34e08-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="34e08-120">Пользователи клиентских приложений могут просматривать содержимое контейнеров адресных книг и, в некоторых случаях, изменять содержимое.</span><span class="sxs-lookup"><span data-stu-id="34e08-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="34e08-121">Контейнеры адресной книги могут создаваться с разными уровнями доступа в зависимости от поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="34e08-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34e08-122">См. также</span><span class="sxs-lookup"><span data-stu-id="34e08-122">See also</span></span>

- [<span data-ttu-id="34e08-123">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="34e08-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)


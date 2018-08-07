---
title: Общие сведения о поставщике MAPI адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4bd64aadd5fc18ba79a8717a5c58df72cd3695ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809684"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="3043b-103">Общие сведения о поставщике MAPI адресной книги</span><span class="sxs-lookup"><span data-stu-id="3043b-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="3043b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3043b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3043b-105">Адресная книга поставщиков маркер доступа к данным каталога.</span><span class="sxs-lookup"><span data-stu-id="3043b-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="3043b-106">Сведения о каталоге состоит из данных для двух типов получателей сообщений: отдельные системы обмена сообщениями пользователями и группами обмена сообщениями пользователей, которые часто адресованное друг с другом в списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="3043b-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="3043b-107">В зависимости от типа получателя и доступа к адресной книге существует большое число сведения, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="3043b-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="3043b-108">Например все поставщиками адресных книг хранить имя, адрес и тип адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="3043b-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="3043b-109">Каждый поставщик адресной книги организует эти данные с помощью одного или нескольких контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3043b-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="3043b-110">Количество и структура контейнеров зависит от реализации поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3043b-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="3043b-111">К примеру один поставщик адресной книги могут использовать один контейнер для хранения всех данных, другой могут использовать один верхнего уровня контейнер, в котором размещается субконтейнеров и третий могут использовать несколько контейнеров верхнего уровня, каждый субконтейнеров создаст.</span><span class="sxs-lookup"><span data-stu-id="3043b-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="3043b-112">Иерархия контейнеров адресной книги может быть весьма вложения. Нет ограничений на номер субконтейнеров, которые могут использоваться.</span><span class="sxs-lookup"><span data-stu-id="3043b-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="3043b-113">На следующем рисунке показана типичная MAPI организация адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3043b-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="3043b-114">**Организация адресной книги**</span><span class="sxs-lookup"><span data-stu-id="3043b-114">**Address book organization**</span></span>
  
<span data-ttu-id="3043b-115">![Организация адресной книги] (media/amapi_04.gif "Организация адресной книги")</span><span class="sxs-lookup"><span data-stu-id="3043b-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="3043b-116">MAPI интегрирует все сведения, предоставляемые поставщиками установленных адресной книги в одном адресную книгу, презентацию объединенные представления для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="3043b-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="3043b-117">Встроенная список верхнего уровня контейнеров, отображаемые каждым поставщиками установленных адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3043b-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="3043b-118">Большинство поставщиками адресных книг предоставлять только несколько контейнеров (обычно один-три) на верхнем уровне для включения в верхний уровень интегрированной адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="3043b-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="3043b-119">Например поставщика адресных книг могут быть недоступны «Все пользователи» и «Локальные пользователи» как два контейнера верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="3043b-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="3043b-120">Пользователи клиентских приложений можно просматривать содержимое контейнеров адресной книги и, в некоторых случаях, измените значение параметра.</span><span class="sxs-lookup"><span data-stu-id="3043b-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="3043b-121">Контейнеры адресной книги может создаваться с использованием различные уровни доступа, в зависимости от доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="3043b-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3043b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3043b-122">See also</span></span>

- [<span data-ttu-id="3043b-123">Функции MAPI и архитектура</span><span class="sxs-lookup"><span data-stu-id="3043b-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)


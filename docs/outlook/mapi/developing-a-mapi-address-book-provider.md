---
title: Разработка поставщика адресной книги MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 731ebf6f61db8e9f425d48ab63cb7b81035a41c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584284"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="a4406-103">Разработка поставщика адресной книги MAPI</span><span class="sxs-lookup"><span data-stu-id="a4406-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="a4406-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4406-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4406-105">Поставщика адресных книг предоставляет сведения о получателях для клиентских приложений, для хранения сообщений и поставщиками, транспорта и MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4406-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="a4406-106">Сведения о получателях является иерархической в секции хранилища, известных как контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a4406-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="a4406-107">Каждые адресной книги в профиле участвует один или более верхнего уровня, или родительских, контейнеров MAPI адресную книгу, интегрированное представление сведения о получателях из всех адресов книги поставщиков в сеансе.</span><span class="sxs-lookup"><span data-stu-id="a4406-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="a4406-108">Это через MAPI адресной книги, что клиенты и других поставщиков услуг получить доступ к данным поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="a4406-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="a4406-109">MAPI выполняет построение интегрированной адресной книги с:</span><span class="sxs-lookup"><span data-stu-id="a4406-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="a4406-110">Извлечение верхнего уровня контейнеры из каждый поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a4406-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="a4406-111">Извлечение таблицы иерархии каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4406-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="a4406-112">Копирование каждой таблицы иерархии в таблицу интегрированной иерархии.</span><span class="sxs-lookup"><span data-stu-id="a4406-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="a4406-113">Это таблица интегрированной иерархии, взаимодействующий с клиента.</span><span class="sxs-lookup"><span data-stu-id="a4406-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="a4406-114">MAPI, задает несколько требований на записи поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a4406-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="a4406-115">Диапазон возможных функций, вы можете реализовать как разнообразные и гибкие записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a4406-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="a4406-116">К примеру ваш поставщик может быть только для указания представления только для чтения определенного типа сведения о получателях или реализации полного набора возможностей, позволяя клиентов или поставщиков добавления или изменения для получателя данных и применяться условия поиска для определения настраиваемых представлений.</span><span class="sxs-lookup"><span data-stu-id="a4406-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="a4406-117">Ваш поставщик данных могут располагаться локально в файле или в базе данных или на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="a4406-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="a4406-118">Некоторые поставщиками адресных книг, предназначенные для работы с конкретной системе обмена сообщениями, тесно связан с поставщиком транспорта, в то время как другие пользователи могут работать с любой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a4406-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="a4406-119">MAPI определяет особый тип называется Личная адресная книга или адресной книги, который реализует один контейнер можно изменить и может содержать сведения о получателях, скопированные из других контейнеров, а также данные, созданные непосредственно поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a4406-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="a4406-120">Несмотря на то, что любые поставщик адресной книги можно реализовать адресной книги и несколько PABs можно добавить в профиль, для работы в качестве личной адресной книги во время любого одного сеанса могут быть обозначены только один из этих поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a4406-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  


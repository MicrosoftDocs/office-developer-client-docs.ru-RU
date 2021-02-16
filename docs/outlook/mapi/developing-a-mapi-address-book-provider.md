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
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409372"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="61856-103">Разработка поставщика адресной книги MAPI</span><span class="sxs-lookup"><span data-stu-id="61856-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="61856-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61856-105">Поставщик адресной книги передает сведения о получателях в клиентские приложения, в хранилище сообщений и поставщикам транспорта, а также в MAPI.</span><span class="sxs-lookup"><span data-stu-id="61856-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="61856-106">Сведения о получателях иерархически организованы в хранилища, известные как контейнеры.</span><span class="sxs-lookup"><span data-stu-id="61856-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="61856-107">Каждая адресная книга в профиле вносит один или несколько контейнеров верхнего уровня или родительских контейнеров в адресную книгу MAPI, интегрированное представление сведений о получателях от всех поставщиков адресных книг в сеансе.</span><span class="sxs-lookup"><span data-stu-id="61856-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="61856-108">Клиенты и другие поставщики услуг получают доступ к данным поставщика адресной книги через адресную книгу MAPI.</span><span class="sxs-lookup"><span data-stu-id="61856-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="61856-109">MAPI создает интегрированную адресную книгу с помощью:</span><span class="sxs-lookup"><span data-stu-id="61856-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="61856-110">Искомые контейнеры верхнего уровня от каждого поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="61856-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="61856-111">Искомая таблица иерархии каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="61856-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="61856-112">Копирование каждой таблицы иерархии в интегрированную таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="61856-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="61856-113">Это интегрированная таблица иерархии, которая является для клиента.</span><span class="sxs-lookup"><span data-stu-id="61856-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="61856-114">MAPI предъявляет несколько требований к авторам поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="61856-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="61856-115">Диапазон возможных функций, которые можно реализовать в качестве автора адресной книги, является разнообразным и гибким.</span><span class="sxs-lookup"><span data-stu-id="61856-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="61856-116">Например, поставщик может быть ограничен представлением сведений о получателях определенного типа только для чтения или реализовать полный набор функций, что, возможно, позволит клиентам или поставщикам внести дополнения или изменения в данные получателя и назначить условия поиска для определения настраиваемых представлений.</span><span class="sxs-lookup"><span data-stu-id="61856-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="61856-117">Данные поставщика могут находиться локально в файле или базе данных или на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="61856-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="61856-118">Некоторые поставщики адресных книг предназначены для работы с определенной системой обмена сообщениями, тесной связи с поставщиком транспорта, а другие могут работать с любой системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="61856-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="61856-119">MAPI определяет особый тип поставщика адресной книги, который называется личной адресной книгой, или PAB, который реализует один из измояемых контейнеров и может удерживать сведения о получателях, скопированные из других контейнеров, а также сведения, созданные напрямую.</span><span class="sxs-lookup"><span data-stu-id="61856-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="61856-120">Хотя любой поставщик адресной книги может реализовать PAB, и в профиль можно добавить несколько таких адресных книг, только один из этих поставщиков может быть назначен для работы в качестве PAB во время одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="61856-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  


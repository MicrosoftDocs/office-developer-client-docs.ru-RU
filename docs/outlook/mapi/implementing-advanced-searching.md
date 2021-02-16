---
title: Реализация расширенных поисков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407391"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="df65b-103">Реализация расширенных поисков</span><span class="sxs-lookup"><span data-stu-id="df65b-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="df65b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df65b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df65b-105">Некоторые контейнеры адресной книги поддерживают расширенный поиск, который позволяет клиентам искать свойства, кроме **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="df65b-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="df65b-106">Для поддержки расширенных поисковых запросов поставщик должен реализовать специальный контейнер, доступный через свойство **PR_SEARCH** ([PidTagSearch)](pidtagsearch-canonical-property.md)других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="df65b-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="df65b-107">**PR_SEARCH** содержит объект контейнера, который предоставляет доступ к таблице отображения, в котором описывается диалоговое окно, используемого для ввода и изменения расширенных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="df65b-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="df65b-108">**Поддержка расширенных поисков**</span><span class="sxs-lookup"><span data-stu-id="df65b-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="df65b-109">Определите свойство для каждого условия поиска.</span><span class="sxs-lookup"><span data-stu-id="df65b-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="df65b-110">В разделе кода в методе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **контейнера,** который обрабатывает PR_SEARCH свойства:</span><span class="sxs-lookup"><span data-stu-id="df65b-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="df65b-111">Убедитесь, что клиент запрашивает **интерфейс IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="df65b-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="df65b-112">Если запрашивается недопустимый интерфейс, сбой и возврат MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="df65b-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="df65b-113">Создайте новый объект поиска, который поддерживает **интерфейс IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="df65b-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="df65b-114">На этом этапе будет выполнен вызов метода **IMAPIProp::OpenProperty** контейнера поиска для получения его свойства **PR_DETAILS_TABLE** ([PidTagDetailsTable).](pidtagdetailstable-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="df65b-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="df65b-115">Поставщик должен предоставить отображаемую таблицу, обычно с помощью вызова [BuildDisplayTable,](builddisplaytable.md)которая описывает диалоговое окно "Расширенный поиск" контейнера.</span><span class="sxs-lookup"><span data-stu-id="df65b-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="df65b-116">MAPI отображает диалоговое окно поиска, позволяя пользователю вводить соответствующие условия.</span><span class="sxs-lookup"><span data-stu-id="df65b-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="df65b-117">Когда пользователь завершит работу, MAPI вызывает метод [контейнера IMAPIProp::SetProps](imapiprop-setprops.md) для хранения критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="df65b-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="df65b-118">Будет выполнен вызов для запроса таблицы содержимого контейнера поиска.</span><span class="sxs-lookup"><span data-stu-id="df65b-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="df65b-119">Заполнять таблицу содержимого всеми записями в контейнере, которые соответствуют условиям.</span><span class="sxs-lookup"><span data-stu-id="df65b-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    


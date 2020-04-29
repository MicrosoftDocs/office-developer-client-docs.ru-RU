---
title: Реализация расширенного поиска
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
# <a name="implementing-advanced-searching"></a><span data-ttu-id="ecba1-103">Реализация расширенного поиска</span><span class="sxs-lookup"><span data-stu-id="ecba1-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="ecba1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecba1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecba1-105">Некоторые контейнеры адресных книг поддерживают функцию расширенного поиска, позволяющую клиентам выполнять поиск по свойствам, отличным от **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecba1-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="ecba1-106">Для поддержки расширенного поиска поставщик должен реализовать специальный контейнер, доступный с помощью свойства **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="ecba1-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="ecba1-107">**PR_SEARCH** содержит объект Container, предоставляющий доступ к отображаемой таблице, в которой описывается диалоговое окно, используемое для ввода и изменения расширенных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="ecba1-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="ecba1-108">**Поддержка расширенного поиска**</span><span class="sxs-lookup"><span data-stu-id="ecba1-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="ecba1-109">Определите свойство для каждого из критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="ecba1-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="ecba1-110">В разделе кода в методе [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , обрабатывающем свойство **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="ecba1-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="ecba1-111">Убедитесь, что клиент запрашивает интерфейс **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="ecba1-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="ecba1-112">Если запрашивается недопустимый интерфейс, происходит ошибка и возвращается MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="ecba1-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="ecba1-113">Создание нового объекта поиска, поддерживающего интерфейс **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="ecba1-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="ecba1-114">На этом шаге будет выполнен вызов метода **IMAPIProp:: опенпроперти** контейнера поиска для получения свойства **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecba1-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="ecba1-115">Поставщик должен предоставить отображаемую таблицу, как правило, с помощью вызова [буилддисплайтабле](builddisplaytable.md), которое описывает диалоговое окно Расширенный поиск контейнера.</span><span class="sxs-lookup"><span data-stu-id="ecba1-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="ecba1-116">MAPI отображает диалоговое окно поиска, которое позволяет пользователю ввести соответствующие условия.</span><span class="sxs-lookup"><span data-stu-id="ecba1-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="ecba1-117">По завершении работы пользователя MAPI вызывает метод контейнера [IMAPIProp:: SetProps](imapiprop-setprops.md) для хранения условий поиска.</span><span class="sxs-lookup"><span data-stu-id="ecba1-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="ecba1-118">Будет выполнен вызов для запроса таблицы содержимого контейнера поиска.</span><span class="sxs-lookup"><span data-stu-id="ecba1-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="ecba1-119">Заполните таблицу содержимого всеми записями в контейнере, которые удовлетворяют критериям.</span><span class="sxs-lookup"><span data-stu-id="ecba1-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    


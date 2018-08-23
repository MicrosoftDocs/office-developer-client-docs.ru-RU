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
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571971"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="a8382-103">Реализация расширенного поиска</span><span class="sxs-lookup"><span data-stu-id="a8382-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="a8382-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8382-105">Некоторые контейнеров адресной книги поддерживает расширенные возможность поиска, который позволяет клиентам для поиска по свойства не **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8382-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="a8382-106">Для поддержки расширенного поиска, поставщик должен реализовывать специальный контейнер, доступен через свойство **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) на других контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a8382-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="a8382-107">**PR_SEARCH** содержит объект контейнера, который предоставляет доступ для отображения таблицы с описанием диалоговое окно для ввода и изменить критерии расширенный поиск.</span><span class="sxs-lookup"><span data-stu-id="a8382-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="a8382-108">**Для поддержки расширенного поиска**</span><span class="sxs-lookup"><span data-stu-id="a8382-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="a8382-109">Определение свойства для каждого из условий поиска.</span><span class="sxs-lookup"><span data-stu-id="a8382-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="a8382-110">В разделе код в метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, который обрабатывает свойство **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="a8382-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="a8382-111">Проверьте, что клиент запрашивает интерфейс **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a8382-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="a8382-112">Если запрашивается несоответствующий интерфейс с ошибкой и возвращают MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="a8382-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="a8382-113">Создайте новый объект поиска, который поддерживает интерфейс **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a8382-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="a8382-114">На этом этапе будет вызов метода **IMAPIProp::OpenProperty** поиска контейнера для получения его свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8382-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="a8382-115">Ваш поставщик необходимо задать отображаемое таблицы, обычно с помощью вызова [BuildDisplayTable](builddisplaytable.md), с описанием диалоговое окно Расширенный поиск контейнера.</span><span class="sxs-lookup"><span data-stu-id="a8382-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="a8382-116">MAPI отображает поле поиска, что пользователю требуется ввести соответствующие условиям.</span><span class="sxs-lookup"><span data-stu-id="a8382-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="a8382-117">После завершения работы пользователя, MAPI вызывает метод [IMAPIProp::SetProps](imapiprop-setprops.md) контейнер для хранения условия поиска.</span><span class="sxs-lookup"><span data-stu-id="a8382-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="a8382-118">Запрос поиска контейнера содержимое таблицы будет выполнен вызов.</span><span class="sxs-lookup"><span data-stu-id="a8382-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="a8382-119">Заполните таблицу содержимого со всеми записей в контейнере, соответствующие критериям.</span><span class="sxs-lookup"><span data-stu-id="a8382-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    


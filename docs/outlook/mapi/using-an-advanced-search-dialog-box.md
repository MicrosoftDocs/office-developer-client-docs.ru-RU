---
title: Использование диалогового окна "Расширенный поиск"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588771"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="62398-103">Использование диалогового окна "Расширенный поиск"</span><span class="sxs-lookup"><span data-stu-id="62398-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="62398-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62398-105">Некоторые контейнеров адресной книги поддерживает расширенные возможность поиска, который позволяет клиентам для поиска по свойства не **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62398-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="62398-106">Контейнеры адресной книги, которые поддерживают расширенный поиск имеют свойство объекта контейнера **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="62398-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="62398-107">Этот объект-контейнер предоставляет доступ для отображения таблицы с описанием диалоговое окно поиска — диалоговое окно используется для ввода и изменить критерии расширенный поиск.</span><span class="sxs-lookup"><span data-stu-id="62398-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="62398-108">**Для выполнения расширенного поиска на контейнер адресной книги**</span><span class="sxs-lookup"><span data-stu-id="62398-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="62398-109">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, указав **PR_SEARCH** для свойства tag и IID_IMAPIContainer для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62398-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="62398-110">Вызовите метод **IMAPIProp::OpenProperty** объекта поиска, задание для свойства tag и IID_IMAPITable **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62398-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="62398-111">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) объект поиска, чтобы установить значения для свойств для использования в расширенный поиск.</span><span class="sxs-lookup"><span data-stu-id="62398-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="62398-112">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объект поиска, чтобы сохранить критерии расширенный поиск.</span><span class="sxs-lookup"><span data-stu-id="62398-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="62398-113">В этом последовательность вызовов приводит к ограничениям, становится доступным, когда клиент вызывает метод **GetSearchCriteria** объекта поиска.</span><span class="sxs-lookup"><span data-stu-id="62398-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  


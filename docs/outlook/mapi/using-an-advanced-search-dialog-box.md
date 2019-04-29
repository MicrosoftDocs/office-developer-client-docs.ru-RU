---
title: Использование диалогового окна "Расширенный Поиск"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437303"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="e2daa-103">Использование диалогового окна "Расширенный Поиск"</span><span class="sxs-lookup"><span data-stu-id="e2daa-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="e2daa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2daa-105">Некоторые контейнеры адресных книг поддерживают функцию расширенного поиска, позволяющую клиентам выполнять поиск по свойствам, отличным от **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2daa-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="e2daa-106">Контейнеры адресных книг, поддерживающие Расширенный поиск, имеют свойство объекта Container с именем **пр_сеарч** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2daa-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="e2daa-107">Этот объект Container предоставляет доступ к таблице отображения, в которой описывается диалоговое окно поиска — диалоговое окно, используемое для ввода и редактирования расширенных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="e2daa-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="e2daa-108">**Выполнение расширенного поиска в контейнере адресной книги**</span><span class="sxs-lookup"><span data-stu-id="e2daa-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="e2daa-109">ВыЗовите метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , указав **пр_сеарч** для тега Property и иид_имапиконтаинер для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2daa-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="e2daa-110">ВыЗовите метод **IMAPIProp:: опенпроперти** объекта Search, указав **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для тега свойства и иид_имапитабле для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2daa-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="e2daa-111">ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) объекта Search для установки значений свойств, которые будут использоваться в расширенном поиске.</span><span class="sxs-lookup"><span data-stu-id="e2daa-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="e2daa-112">ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) объекта Search для сохранения расширенных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="e2daa-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="e2daa-113">Эта последовательность вызовов приводит к ограничению, которое доступно, когда клиент вызывает метод **жетсеарчкритериа** объекта поиска.</span><span class="sxs-lookup"><span data-stu-id="e2daa-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  


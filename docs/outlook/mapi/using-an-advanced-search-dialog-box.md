---
title: Использование диалоговой окне расширенный поиск
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
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="58f03-103">Использование диалоговой окне расширенный поиск</span><span class="sxs-lookup"><span data-stu-id="58f03-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="58f03-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58f03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58f03-105">Некоторые контейнеры адресных книг поддерживают расширенные возможности поиска, которые позволяют  клиентам искать свойства, не PR_DISPLAY_NAME[(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="58f03-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="58f03-106">Контейнеры адресной книги, поддерживают расширенный поиск, имеют свойство объекта контейнера **PR_SEARCH** [(PidTagSearch).](pidtagsearch-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="58f03-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="58f03-107">Этот объект контейнера предоставляет доступ к таблице отображения, которая описывает диалоговое окно поиска — диалоговое окно, используемого для ввода и редактирования расширенных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="58f03-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="58f03-108">**Выполнение расширенных поисков в контейнере адресной книги**</span><span class="sxs-lookup"><span data-stu-id="58f03-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="58f03-109">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера,  указав PR_SEARCH для тега свойства и IID_IMAPIContainer для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58f03-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="58f03-110">Вызов метода **IMAPIProp::OpenProperty** объекта поиска с указанием **PR_DETAILS_TABLE** [(PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)для тега свойства и IID_IMAPITable для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58f03-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="58f03-111">Вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) объекта поиска, чтобы установить значения свойств, которые будут использоваться в продвинутом поиске.</span><span class="sxs-lookup"><span data-stu-id="58f03-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="58f03-112">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта поиска, чтобы сохранить расширенные критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="58f03-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="58f03-113">Эта последовательность вызовов приводит к ограничению, когда клиент вызывает метод **GetSearchCriteria** объекта поиска.</span><span class="sxs-lookup"><span data-stu-id="58f03-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  


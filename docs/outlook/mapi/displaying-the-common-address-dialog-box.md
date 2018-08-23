---
title: Отображение диалогового окна общего адреса
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 00d1063310aaf1a8948e04d725d7e11418cf986c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592425"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="81901-103">Отображение диалогового окна общего адреса</span><span class="sxs-lookup"><span data-stu-id="81901-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="81901-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81901-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81901-105">Диалоговое окно MAPI распространенных адрес может использоваться для различных адресации задачи, такие как создание списка получателей.</span><span class="sxs-lookup"><span data-stu-id="81901-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="81901-106">Чтобы отобразить это диалоговое окно, вызовите **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="81901-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="81901-107">В зависимости от того, какой из много параметров, заданную вами и как задать можно ограничить экрана записи определенного типа из конкретного контейнера.</span><span class="sxs-lookup"><span data-stu-id="81901-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="81901-108">**Чтобы ограничить поле адрес для отображения только запись адресной книги (адресной книги)**</span><span class="sxs-lookup"><span data-stu-id="81901-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="81901-109">Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="81901-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="81901-110">Создание ограничение свойство, которое использует RELOP_EQ для элемента **relop** структура [SPropertyRestriction](spropertyrestriction.md) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) в качестве член **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="81901-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="81901-111">Если вы используете **PR_ENTRYID**, передайте идентификатор записи, извлекается из **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="81901-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="81901-112">Если вы используете **PR_AB_PROVIDER_ID**, передайте значение, включенные в MSPAB. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="81901-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="81901-113">**PR_AB_PROVIDER_ID** — уникальный идентификатор для адресной книги, разработанная MAPI.</span><span class="sxs-lookup"><span data-stu-id="81901-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="81901-114">Вызов [IAddrBook::Address](iaddrbook-address.md) совместно с параметром _lpHierRestriction_ с указанием ограничении свойства.</span><span class="sxs-lookup"><span data-stu-id="81901-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    


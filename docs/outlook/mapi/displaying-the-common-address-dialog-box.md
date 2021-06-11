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
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436905"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="6548b-103">Отображение диалогового окна общего адреса</span><span class="sxs-lookup"><span data-stu-id="6548b-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="6548b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6548b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6548b-105">Диалоговое окно общего адреса MAPI можно использовать для решения различных задач, таких как создание списка получателей.</span><span class="sxs-lookup"><span data-stu-id="6548b-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="6548b-106">Чтобы отобразить диалоговое окно, позвоните **в IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="6548b-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="6548b-107">В зависимости от того, какой из множества параметров и как вы их заданы, вы можете ограничить отображение записей определенного типа из определенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="6548b-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="6548b-108">**Ограничение диалоговых окне адресов только отображением записей личной адресной книги (PAB)**</span><span class="sxs-lookup"><span data-stu-id="6548b-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="6548b-109">Вызов [IAddrBook::GetPAB](iaddrbook-getpab.md) для получения идентификатора записи PAB.</span><span class="sxs-lookup"><span data-stu-id="6548b-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="6548b-110">Создайте ограничение свойств, RELOP_EQ для  повторного члена [структуры SPropertyRestriction](spropertyrestriction.md)  и PR_ENTRYID [(PidTagEntryId)](pidtagentryid-canonical-property.md)или **PR_AB_PROVIDER_ID** [(PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)в качестве члена **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="6548b-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="6548b-111">Если вы используете **PR_ENTRYID,** передай идентификатор записи, извлеченный из **GetPAB.**</span><span class="sxs-lookup"><span data-stu-id="6548b-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="6548b-112">Если вы используете **PR_AB_PROVIDER_ID,** передай значение, включенного в MSPAB. Файл заглавной папки H.</span><span class="sxs-lookup"><span data-stu-id="6548b-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="6548b-113">**PR_AB_PROVIDER_ID** является уникальным идентификатором для PAB, разработанного MAPI.</span><span class="sxs-lookup"><span data-stu-id="6548b-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="6548b-114">Вызов [IAddrBook::Address](iaddrbook-address.md) с параметром  _lpHierRestriction,_ указывающий на ограничение свойства.</span><span class="sxs-lookup"><span data-stu-id="6548b-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    


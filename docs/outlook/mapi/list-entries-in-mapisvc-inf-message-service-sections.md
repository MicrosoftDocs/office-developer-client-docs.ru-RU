---
title: Список записей в разделах службы сообщений MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435931"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="d6d08-103">Список записей в разделах службы сообщений MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="d6d08-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="d6d08-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6d08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6d08-105">Существует два типа записей в списке разделов: один содержит разделы поставщика услуг, а второй — различные разделы, специфичные для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="d6d08-106">Эти два типа записей отображаются в mapisvc.inf в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="d6d08-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="d6d08-107">Каждый раздел  в записи "Поставщики" сопо карту с отдельным разделом, предоставляющим сведения о конфигурации для поставщика услуг, который принадлежит службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="d6d08-108">Каждый раздел в **записи "Разделы"** сопоподобие раздела, который содержит дополнительные сведения о конфигурации, необходимые службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="d6d08-109">Реализации службы сообщений определяют дополнительные разделы, если они хотят включить специальную информацию, которая не помещается в стандартные разделы.</span><span class="sxs-lookup"><span data-stu-id="d6d08-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="d6d08-110">Службы сообщений со сложными конфигурациями обычно используют запись **Sections** для добавления дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="d6d08-111">В каждом разделе "Службы сообщений" есть запись **"Поставщики"** с по крайней мере одним разделом в списке; Не во всех разделах службы сообщений есть **запись "Разделы".**</span><span class="sxs-lookup"><span data-stu-id="d6d08-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="d6d08-112">Два примера разделов службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="d6d08-113">Первый раздел посвящен службе адресной книги по умолчанию, которая ранее была простой службой сообщений с одним поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="d6d08-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="d6d08-114">Второй раздел посвящен службе MsgService, более сложной службе сообщений с тремя поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="d6d08-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

<span data-ttu-id="d6d08-115">Запись **"Разделы"** в разделе **[MsgService]** содержит два дополнительных раздела, один из них **называется [First_Special_Section],** а другой **— [Second_Special_Section].**</span><span class="sxs-lookup"><span data-stu-id="d6d08-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="d6d08-116">Данные, которые могут отображаться в дополнительных разделах, важны для конкретной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6d08-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="d6d08-117">В следующих разделах показано, как проиллюстрировать дополнительные разделы.</span><span class="sxs-lookup"><span data-stu-id="d6d08-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



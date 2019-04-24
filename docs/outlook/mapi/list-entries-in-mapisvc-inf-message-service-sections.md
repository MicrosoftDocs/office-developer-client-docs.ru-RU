---
title: Список записей в разделах службы сообщений MapiSvc. INF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307835"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="4fc41-103">Список записей в разделах службы сообщений MapiSvc. INF</span><span class="sxs-lookup"><span data-stu-id="4fc41-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="4fc41-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc41-105">Существует два типа записей списка разделов: один, который содержит список разделов поставщиков услуг и один, в котором перечислены разделы, относящиеся к службе различных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fc41-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="4fc41-106">Эти два типа записей отображаются в Mapisvc. INF в следующих форматах:</span><span class="sxs-lookup"><span data-stu-id="4fc41-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="4fc41-107">Каждый раздел в записи **providers** соответствует отдельному разделу, который предоставляет сведения о конфигурации для поставщика услуг, принадлежащего службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fc41-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="4fc41-108">Каждый раздел записи **Sections** соответствует разделу, содержащему дополнительные сведения о конфигурации, необходимые службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fc41-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="4fc41-109">Помощник по внедрению службы сообщений определяет дополнительные разделы, чтобы включить особые сведения, не соответствующие стандартным разделам.</span><span class="sxs-lookup"><span data-stu-id="4fc41-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="4fc41-110">Службы сообщений с сложными конфигурациями обычно используют запись **разделов** для добавления дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="4fc41-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="4fc41-111">Каждый раздел служб сообщений содержит запись " **поставщики** " по крайней мере с одним разделом в списке; не все разделы службы сообщений содержат запись **разделов** .</span><span class="sxs-lookup"><span data-stu-id="4fc41-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="4fc41-112">Ниже приведены два примера разделов службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fc41-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="4fc41-113">Первый раздел предназначен для службы адресной книги по умолчанию с предыдущей иллюстрации, простой службы сообщений с одним поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="4fc41-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="4fc41-114">Второй раздел предназначен для службы Мсгсервице, более сложной учебной службы сообщений с тремя поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="4fc41-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="4fc41-115">Запись **Sections** в разделе **[мсгсервице]** содержит два дополнительных раздела, один из которых называется **[фирст_спеЦиал_сектион]** , а другой — **[секонд_спеЦиал_сектион]**.</span><span class="sxs-lookup"><span data-stu-id="4fc41-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="4fc41-116">Данные, которые могут отображаться в дополнительных разделах, являются значимыми для конкретной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fc41-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="4fc41-117">Для иллюстрации дополнительных разделов отображаются следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="4fc41-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



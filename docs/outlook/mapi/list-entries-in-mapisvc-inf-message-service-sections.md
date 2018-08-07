---
title: Записи списков в разделах службы сообщений MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cfb06e8dd305add6049d035c44685be047dc744f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809648"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="95807-103">Записи списков в разделах службы сообщений MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="95807-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="95807-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95807-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95807-105">Существует два типа записей списка раздел: один, в котором приведены разделы поставщика службы и еще один, в котором приведены разделы конкретной службы прочие сообщения.</span><span class="sxs-lookup"><span data-stu-id="95807-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="95807-106">Эти два типа записи отображаются в mapisvc.inf, с помощью следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="95807-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="95807-107">Каждый раздел запись **поставщиков** сопоставляет отдельный раздел, предоставление сведений о конфигурации поставщика услуг, к которой принадлежит служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="95807-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="95807-108">Каждый раздел в **разделах** запись сопоставляет раздел, в котором содержатся сведения о дополнительной настройки, необходимая для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="95807-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="95807-109">Специалистов по внедрению службы сообщений определяется дополнительные разделы, если требуется включить в особые сведения, которые не помещаются в стандартные разделы.</span><span class="sxs-lookup"><span data-stu-id="95807-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="95807-110">Службы сообщений, которые обычно сложных конфигураций использовать запись **разделы** для добавления дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="95807-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="95807-111">Каждый раздел служб сообщение имеет запись **поставщиков** с по крайней мере один раздел в списке; не все разделы сообщения службы имеют записи в **разделах** .</span><span class="sxs-lookup"><span data-stu-id="95807-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="95807-112">Следуйте два примера разделах службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="95807-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="95807-113">Первый раздел — служба по умолчанию адресной книги из более ранних рисунка, служба просто сообщений с одним поставщиком.</span><span class="sxs-lookup"><span data-stu-id="95807-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="95807-114">Второй раздел предназначен для службы MsgService более сложных службы сообщений пример с тремя поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="95807-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="95807-115">Запись **разделов** в разделе **[MsgService]** содержит два дополнительных раздела, один называемое **[First_Special_Section]** и другой вызов **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="95807-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="95807-116">Данные, которые могут отображаться в дополнительных разделах может применяться к службе конкретное сообщение.</span><span class="sxs-lookup"><span data-stu-id="95807-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="95807-117">В этих разделах отображаются следующие дополнительные разделы иллюстрируют.</span><span class="sxs-lookup"><span data-stu-id="95807-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



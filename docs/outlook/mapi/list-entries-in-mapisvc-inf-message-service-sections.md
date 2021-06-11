---
title: Записи списка в разделах Службы сообщений MapiSvc.inf
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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Записи списка в разделах Службы сообщений MapiSvc.inf

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует два типа записей списка разделов: один, в который перечислены разделы поставщика услуг, и один, в который перечислены различные разделы службы сообщений. Эти два типа записей отображаются в mapisvc.inf с помощью следующих форматов:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Каждый раздел в **записи Поставщики** карт в отдельный раздел, предоставляющий сведения о конфигурации для поставщика услуг, который принадлежит к службе сообщений. Каждый раздел в **разделах** записи содержит дополнительные сведения о конфигурации, необходимые службе сообщений. Реализутели службы сообщений определяют дополнительные разделы, если они хотят включить специальную информацию, не вписываемую в стандартные разделы. Службы сообщений со сложными конфигурациями обычно используют запись **Разделы** для добавления дополнительных сведений. В каждом разделе служб сообщений есть запись **Поставщики** с по крайней мере одним разделом в списке; Не во всех разделах службы сообщений есть **запись Разделы.** 
  
Следуют два примера разделов службы сообщений. Первый раздел для службы адресной книги по умолчанию из предыдущей иллюстрации, простой службы сообщений с одним поставщиком услуг. Второй раздел — это служба MsgService , более сложная примерная служба сообщений с тремя поставщиками услуг. 
  
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

В **разделе Разделы** **в разделе [MsgService]** перечислены два дополнительных раздела, один из них называется **[First_Special_Section],** а другой — **[Second_Special_Section].** Данные, которые могут отображаться в дополнительных разделах, важны для конкретной службы сообщений. Эти разделы отображаются ниже, чтобы проиллюстрировать дополнительные разделы. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



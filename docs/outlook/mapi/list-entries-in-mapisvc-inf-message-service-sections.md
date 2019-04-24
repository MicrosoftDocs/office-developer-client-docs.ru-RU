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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Список записей в разделах службы сообщений MapiSvc. INF

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует два типа записей списка разделов: один, который содержит список разделов поставщиков услуг и один, в котором перечислены разделы, относящиеся к службе различных сообщений. Эти два типа записей отображаются в Mapisvc. INF в следующих форматах:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Каждый раздел в записи **providers** соответствует отдельному разделу, который предоставляет сведения о конфигурации для поставщика услуг, принадлежащего службе сообщений. Каждый раздел записи **Sections** соответствует разделу, содержащему дополнительные сведения о конфигурации, необходимые службе сообщений. Помощник по внедрению службы сообщений определяет дополнительные разделы, чтобы включить особые сведения, не соответствующие стандартным разделам. Службы сообщений с сложными конфигурациями обычно используют запись **разделов** для добавления дополнительной информации. Каждый раздел служб сообщений содержит запись " **поставщики** " по крайней мере с одним разделом в списке; не все разделы службы сообщений содержат запись **разделов** . 
  
Ниже приведены два примера разделов службы сообщений. Первый раздел предназначен для службы адресной книги по умолчанию с предыдущей иллюстрации, простой службы сообщений с одним поставщиком услуг. Второй раздел предназначен для службы Мсгсервице, более сложной учебной службы сообщений с тремя поставщиками услуг. 
  
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

Запись **Sections** в разделе **[мсгсервице]** содержит два дополнительных раздела, один из которых называется **[фирст_спеЦиал_сектион]** , а другой — **[секонд_спеЦиал_сектион]**. Данные, которые могут отображаться в дополнительных разделах, являются значимыми для конкретной службы сообщений. Для иллюстрации дополнительных разделов отображаются следующие разделы. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



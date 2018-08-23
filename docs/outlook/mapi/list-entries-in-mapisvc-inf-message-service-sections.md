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
ms.openlocfilehash: c5b5c468b56e5b34d265e7f00bbee96142a88e1c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591123"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Записи списков в разделах службы сообщений MapiSvc.inf

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Существует два типа записей списка раздел: один, в котором приведены разделы поставщика службы и еще один, в котором приведены разделы конкретной службы прочие сообщения. Эти два типа записи отображаются в mapisvc.inf, с помощью следующих форматов:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Каждый раздел запись **поставщиков** сопоставляет отдельный раздел, предоставление сведений о конфигурации поставщика услуг, к которой принадлежит служба сообщений. Каждый раздел в **разделах** запись сопоставляет раздел, в котором содержатся сведения о дополнительной настройки, необходимая для службы сообщений. Специалистов по внедрению службы сообщений определяется дополнительные разделы, если требуется включить в особые сведения, которые не помещаются в стандартные разделы. Службы сообщений, которые обычно сложных конфигураций использовать запись **разделы** для добавления дополнительных сведений. Каждый раздел служб сообщение имеет запись **поставщиков** с по крайней мере один раздел в списке; не все разделы сообщения службы имеют записи в **разделах** . 
  
Следуйте два примера разделах службы сообщений. Первый раздел — служба по умолчанию адресной книги из более ранних рисунка, служба просто сообщений с одним поставщиком. Второй раздел предназначен для службы MsgService более сложных службы сообщений пример с тремя поставщиков услуг. 
  
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

Запись **разделов** в разделе **[MsgService]** содержит два дополнительных раздела, один называемое **[First_Special_Section]** и другой вызов **[Second_Special_Section]**. Данные, которые могут отображаться в дополнительных разделах может применяться к службе конкретное сообщение. В этих разделах отображаются следующие дополнительные разделы иллюстрируют. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```



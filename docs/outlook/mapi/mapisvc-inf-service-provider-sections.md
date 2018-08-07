---
title: Разделы поставщика службы MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ad6a4661025dfd8cbd39d8f58a36d94ab997ada2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809914"
---
# <a name="mapisvcinf-service-provider-sections"></a>Разделы поставщика службы MapiSvc.inf

**Относится к**: Outlook 
  
Mapisvc.inf включает в себя один раздел поставщика службы для каждой записи, указанные в запись **поставщиков** в предыдущем разделе служб сообщения. Разделы поставщика **службы** аналогичны разделах службы сообщений в обоих типов разделы содержат записи в следующем формате: 
  
**свойство tag** = значение свойства 
  
Тем не менее разделах службы сообщений и разделах поставщика службы отличаются, такие свойства операции — это единственный тип операции, содержатся в разделах поставщика службы. Может быть без дополнительных или связанные разделы для поставщиков услуг; все сведения о поставщике услуг должен содержаться в один раздел. 
  
Некоторые свойства, в разделах службы сообщений также задан в разделах поставщика службы, так как эти свойства смысла для них. Свойство **PR_DISPLAY_NAME** приведен пример. Поставщиков услуг и службы сообщений иметь имя, которое используется для отображения в пользовательском интерфейсе конфигурации. В зависимости от поставщика услуг это имя может или не может быть одинаковым. Другие свойства специфичны для поставщиков услуг. 
  
Разделы поставщика обычной службы включают следующие записи, каждый из которых являются обязательными:
  
**PR_DISPLAY_NAME** =  _строки_
  
**PR_PROVIDER_DISPLAY** =  _строки_
  
**PR_PROVIDER_DLL_NAME** =  _имя DLL-файла_
  
**PR_RESOURCE_TYPE** =  _времени_
  
**PR_RESOURCE_FLAGS** =  _битовой маски_
  
Запись **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) похож на **PR_SERVICE_DLL_NAME**; Указывает имя файла для библиотеки DLL, которая содержит поставщика услуг. Код сообщения службы могут храниться в одном из его поставщиков услуг в один и тот же файл DLL или существовать в качестве отдельной библиотеке DLL. Обратите внимание на то, что не суффикс включается в запись вне зависимости от целевой платформы; Отвечает за MAPI добавляется суффикс, если это необходимо. 
  
**PR_RESOURCE_TYPE** Запись ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) представляет тип поставщика услуг; Поставщики услуг установить соответствующий предварительно определенная константа. Допустимые значения включают MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER и MAPI_AB_PROVIDER.
  
Другой записи свойства, которое применяется к службы сообщений и поставщиков услуг, запись **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) указывает параметры. Параметры для этой записи свойство может отличаться в зависимости от поставщика услуг. Например некоторые поставщики хранилища сообщений может значение **PR_RESOURCE_FLAGS** STATUS_NO_DEFAULT_STORE если они никогда не могут работать как хранилище сообщений по умолчанию. 
  
Выполните три примера разделах поставщика службы. В разделе **[AB поставщика]** — раздел поставщика службы для службы адресной книги по умолчанию. В разделах **[MsgService Prov1]** и **[MsgService Prov2]** принадлежат мои собственные службы; раздел поставщик адресной книги — это первый и второй — раздел поставщика хранилища сообщений. 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```



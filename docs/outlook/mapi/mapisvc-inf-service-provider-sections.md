---
title: Разделы поставщиков услуг MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405564"
---
# <a name="mapisvcinf-service-provider-sections"></a>Разделы поставщиков услуг MapiSvc.inf

**Область применения**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf включает один раздел поставщика услуг для каждого из записей, перечисленных в записи **Поставщики** в предыдущем разделе служб сообщений. **Разделы** поставщика услуг похожи на разделы службы сообщений, в которых оба типа разделов содержат записи в этом формате: 
  
**тег свойства** = значение свойства 
  
Однако разделы поставщиков услуг и разделы службы сообщений отличаются тем, что такие записи свойств являются единственным типом записей, включенных в разделы поставщика услуг. Не может быть дополнительных или связанных разделов для поставщиков услуг; вся информация поставщика услуг должна содержаться в одном разделе. 
  
Некоторые свойства, замещение в разделах службы сообщений, также замещение в разделах поставщика услуг, так как эти свойства имеют смысл для обоих. Свойство **PR_DISPLAY_NAME** является примером. Как поставщики услуг, так и службы сообщений имеют имя, которое используется для отображения в пользовательском интерфейсе конфигурации. В зависимости от поставщика услуг это имя может быть одно и то же. Другие свойства являются специфическими для поставщиков услуг. 
  
Типичные разделы поставщика услуг включают следующие записи, все из которых требуются:
  
**PR_DISPLAY_NAME**  =   _строка_
  
**PR_PROVIDER_DISPLAY**  =   _строка_
  
**PR_PROVIDER_DLL_NAME**  =   _имя файла DLL_
  
**PR_RESOURCE_TYPE**  =   _long_
  
**PR_RESOURCE_FLAGS**  =   _bitmask_
  
Запись **PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)похожа на **PR_SERVICE_DLL_NAME;** он указывает имя файла для DLL, который содержит поставщика услуг. Код службы сообщений может храниться у одного из поставщиков услуг в том же файле DLL или существовать в качестве отдельного DLL. Обратите внимание, что суффикс не включен в запись независимо от целевой платформы; MAPI позаботится о добавлении суффикса при необходимости. 
  
**PR_RESOURCE_TYPE** [(Запись PidTagResourceType)](pidtagresourcetype-canonical-property.md)представляет тип поставщика услуг; Поставщики услуг задают ему соответствующую предопределяемую константу. Допустимые значения включают MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER и MAPI_AB_PROVIDER.
  
Другая запись свойства, которая применяется как к службам  сообщений, так и к поставщикам услуг, PR_RESOURCE_FLAGS[(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)указывает параметры. Параметры для этой записи свойства могут отличаться в зависимости от поставщика услуг. Например, некоторые поставщики магазинов  сообщений могут PR_RESOURCE_FLAGS STATUS_NO_DEFAULT_STORE, если они никогда не смогут работать как хранилище сообщений по умолчанию. 
  
Следуют три примера разделов поставщиков услуг. Раздел **[ПОСТАВЩИК AB]** — это раздел поставщика услуг для службы адресной книги по умолчанию. Разделы **[MsgService Prov1]** и **[MsgService Prov2]** принадлежат к my Own Service; Первый — это раздел поставщика адресных книг, а второй — раздел поставщика для хранения сообщений. 
  
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



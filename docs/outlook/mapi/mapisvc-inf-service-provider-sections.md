---
title: Разделы поставщика служб MapiSvc.inf
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
# <a name="mapisvcinf-service-provider-sections"></a>Разделы поставщика служб MapiSvc.inf

**Относится к**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf содержит один раздел поставщика услуг для каждой записи, перечисленной в записи **Поставщики** в предыдущем разделе служб сообщений. **Разделы** поставщика услуг похожи на разделы службы сообщений, так как оба типа разделов содержат записи в этом формате: 
  
**тег свойства** = значение свойства 
  
Однако разделы поставщика услуг и разделы службы сообщений отличаются тем, что такие записи свойств являются единственным типом записи, включенной в разделы поставщика услуг. Для поставщиков услуг не может быть дополнительных или связанных разделов; Все сведения о поставщике услуг должны содержаться в одном разделе. 
  
Некоторые свойства, установленные в разделах службы сообщений, также замещение в разделах поставщика услуг, так как эти свойства имеют смысл для обоих. Примером **PR_DISPLAY_NAME** является свойство PR_DISPLAY_NAME. Как поставщики услуг, так и службы сообщений имеют имя, которое используется для отображения в пользовательском интерфейсе конфигурации. В зависимости от поставщика услуг это имя может быть или не быть одинаковым. Другие свойства являются специфическими для поставщиков услуг. 
  
Типичные разделы поставщиков услуг включают следующие записи, все из которых являются обязательной:
  
**PR_DISPLAY_NAME**  =   _string_
  
**PR_PROVIDER_DISPLAY**  =   _string_
  
**PR_PROVIDER_DLL_NAME**  =   _имя DLL-файла_
  
**PR_RESOURCE_TYPE**  =   _long_
  
**PR_RESOURCE_FLAGS**  =   _битоваяmask_
  
Запись **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)аналогична **PR_SERVICE_DLL_NAME;** он указывает имя файла для DLL, которая содержит поставщика услуг. Код службы сообщений может храниться у одного из поставщиков услуг в том же DLL-файле или существовать как отдельная DLL. Обратите внимание, что суффикс не включен в запись независимо от целевой платформы; MAPI при необходимости добавляет суффикс. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) представляет тип поставщика услуг; поставщики услуг присваивают ему соответствующую предопределеную константу. Допустимые значения: MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER и MAPI_AB_PROVIDER.
  
Другая запись свойства, которая применяется как к службам сообщений, так и к поставщикам служб, PR_RESOURCE_FLAGS **(** [PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)указывает параметры. Параметры для этой записи свойства могут отличаться в зависимости от поставщика услуг. Например, некоторые поставщики  store сообщений могут PR_RESOURCE_FLAGS значение STATUS_NO_DEFAULT_STORE, если они никогда не смогут работать как хранилище сообщений по умолчанию. 
  
В этом примере следуют три примера разделов поставщика услуг. Раздел **[Поставщик ab]** — это раздел поставщика услуг для службы адресной книги по умолчанию. Разделы **[MsgService Prov1]** и **[MsgService Prov2]** относятся к моей собственной службе; Первый раздел является разделом поставщика адресной книги, а второй — разделом поставщика службы хранения сообщений. 
  
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



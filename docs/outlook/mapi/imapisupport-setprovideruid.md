---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: df842e633f1586d6d77441126d51b2ce44ec3beb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589072"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует [MAPIUID](mapiuid.md) структуры, который уникальным образом представляет поставщика услуг. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpProviderID_
  
> [in] Указатель на структуру **MAPIUID** , идентифицирующий поставщика хранилища адресной книги или сообщения. 
    
 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Структура **MAPIUID** успешно зарегистрированы. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::SetProviderUID** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки. Эти поставщики вызов **SetProviderUID** для регистрации уникальный идентификатор, описанного в структуре **MAPIUID** , который указывает _lpProviderID_. Поставщики включают этот идентификатор в все идентификаторы записи, которые они создают. 
  
MAPI использует структуру **MAPIUID** при отправке исходящих сообщений в очередь MAPI и для определения соответствующего поставщика для обработки запросов клиентов. Например когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI проверяет **MAPIUID** часть идентификатор записи, сопоставляет его с поставщиком, который передается **SetProviderUID**и вызывает его **OpenEntry** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SetProviderUID** во время входа для регистрации структуры **MAPIUID** . MAPI позволяет адресной книги и сообщения поставщиков хранилища для регистрации несколько идентификаторов. При внесении нескольких звонков на **SetProviderUID**всегда Добавление структуры **MAPIUID** набору поставщика **MAPIUID** структуры, даже в том случае, если **MAPIUID** уже существует. **SetProviderUID** нельзя удалить **MAPIUID**. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


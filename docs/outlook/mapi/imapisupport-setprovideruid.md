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
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809169"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Относится к**: Outlook 
  
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Структура **MAPIUID** успешно зарегистрированы. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::SetProviderUID** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки. Эти поставщики вызов **SetProviderUID** для регистрации уникальный идентификатор, описанного в структуре **MAPIUID** , который указывает _lpProviderID_. Поставщики включают этот идентификатор в все идентификаторы записи, которые они создают. 
  
MAPI использует структуру **MAPIUID** при отправке исходящих сообщений в очередь MAPI и для определения соответствующего поставщика для обработки запросов клиентов. Например когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI проверяет **MAPIUID** часть идентификатор записи, сопоставляет его с поставщиком, который передается **SetProviderUID**и вызывает его **OpenEntry** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SetProviderUID** во время входа для регистрации структуры **MAPIUID** . MAPI позволяет адресной книги и сообщения поставщиков хранилища для регистрации несколько идентификаторов. При внесении нескольких звонков на **SetProviderUID**всегда Добавление структуры **MAPIUID** набору поставщика **MAPIUID** структуры, даже в том случае, если **MAPIUID** уже существует. **SetProviderUID** нельзя удалить **MAPIUID**. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


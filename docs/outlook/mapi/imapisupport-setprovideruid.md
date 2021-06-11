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
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437541"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует [структуру MAPIUID,](mapiuid.md) которая однозначно представляет поставщика услуг. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpProviderID_
  
> [in] Указатель на структуру **MAPIUID,** которая определяет адресную книгу или поставщика магазина сообщений. 
    
 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Структура **MAPIUID** успешно зарегистрирована. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::SetProviderUID** реализован для объектов поддержки поставщиков адресной книги и магазина сообщений. Эти поставщики звонят **SetProviderUID** для регистрации уникального идентификатора, описанного в структуре **MAPIUID,** на который указывает _lpProviderID._ Поставщики включают этот идентификатор во все идентификаторы записи, которые они создают. 
  
MapI использует структуру **MAPIUID,** когда отправляет исходящие сообщения в пулер MAPI и определяет подходящего поставщика для обработки запросов клиентов. Например, когда клиент вызывает метод [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI проверяет часть **MAPIUID** идентификатора входа, передает ее поставщику, передав его **SetProviderUID,** и вызывает **openEntry** этого поставщика. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SetProviderUID во** время регистрации **структуры MAPIUID.** MAPI позволяет поставщикам адресных книг и магазинов сообщений регистрировать несколько идентификаторов. При многократном вызове **в SetProviderUID** структура **MAPIUID** всегда добавляется в набор структур **MAPIUID** поставщика, даже если **MAPIUID** является дубликатом. **SetProviderUID** не может удалить **MAPIUID.** 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


---
title: имсгсервицеадминадминпровидерс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422763"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Параметры

 _лпуид_
  
> возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для контролируемой службы сообщений. 
    
 _ulFlags_
  
> возврата Всегда имеет значение NULL. 
    
 _лпппровидерадмин_
  
> вышли Указатель на указатель на объект администрирования поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект администрирования поставщика успешно возвращен.
    
MAPI_E_NOT_FOUND 
  
> **Мапиуид** , на который указывает _лпуид_ , не существует. 
    
## <a name="remarks"></a>Примечания

Метод **имсгсервицеадмин:: админпровидерс** предоставляет доступ к объекту администрирования поставщика. Администрирование поставщика — это объект, который поддерживает интерфейс [ипровидерадмин](iprovideradminiunknown.md) и позволяет клиентам выполнять следующие действия: 
  
- Добавление поставщиков служб в службу сообщений.
    
- Удаление поставщиков услуг из службы сообщений.
    
- Откройте разделы профилей.
    
- Доступ к таблице поставщика службы сообщений.
    
Типы изменений, которые могут быть применены к службе сообщений в то время, когда профиль используется, зависят от службы сообщений. Однако большинство служб сообщений не поддерживают такие изменения, как добавление и удаление поставщиков при использовании профиля.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить структуру **мапиуид** для службы сообщений для администрирования, извлеките столбец свойств **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки службы сообщений в таблице службы сообщений. Для получения дополнительных сведений обратитесь к процедуре, описанной в методе [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мсгсервицетабледлг. cpp  <br/> |Кмсгсервицетабледлг:: Ондисплайитем  <br/> |MFCMAPI использует метод **имсгсервицеадмин:: админпровидерс** , чтобы открыть объект администрирования поставщика для службы.  <br/> |
   
## <a name="see-also"></a>См. также



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


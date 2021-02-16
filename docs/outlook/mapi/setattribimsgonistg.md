---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428832"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленного функцией [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики store сообщений  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Параметры

 _lpObject_
  
> [in] Указатель на объект, для которого устанавливаются атрибуты свойства. 
    
 _lpPropTags_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) содержащую массив тегов свойств, указывающих свойства, для которых устанавливаются атрибуты свойства. 
    
 _lpPropAttrs_
  
> [in] Указатель на [структуру SPropAttrArray](spropattrarray.md) со списком атрибутов свойств, которые необходимо установить. 
    
 _lppPropProblems_
  
> [out] Указатель на возвращенную [структуру SPropProblemArray,](spropproblemarray.md) содержащую набор проблем со свойствами. Эта структура определяет проблемы, которые возникают, если **setAttribIMsgOnIStg** удалось установить некоторые свойства, но не все. Если указатель на NULL передается в  _параметре lppPropProblems,_ массив проблем свойств не возвращается, даже если некоторые свойства не заданы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов в целом был успешным, но не удалось получить доступ к одному или более свойствам, и он был возвращен с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Примечания

Доступ к атрибутам свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для объекта OLE структурированного хранилища, [OpenIMsgOnIStg](openimsgonistg.md) создает объект [IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта OLE **IStorage.** Атрибуты свойств для таких объектов можно установить или изменить с помощью **SetAttribIMsgOnIStg** и получить с помощью [GetAttribIMsgOnIStg.](getattribimsgonistg.md) 
  
 **Обратите** внимание, что **getAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают не на всех **объектах IMessage.** Они действительны только для **объектов IMessage**-on-IStorage, возвращенных **OpenIMsgOnIStg.**  
  
В параметре _lpPropAttrs_ число и положение атрибутов должны совпадать с числом и положением тегов свойств, переданных в _параметре lpPropTags._ 
  
Функция **SetAttribIMsgOnIStg** используется для того, чтобы свойства сообщений были только для чтения, если этого требует схема **IMessage.** Для этой цели используется пример поставщика store сообщений. Дополнительные сведения см. [в сообщении.](mapi-messages.md) 
  


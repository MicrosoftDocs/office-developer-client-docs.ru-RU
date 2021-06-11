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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленного функцией [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики магазинов сообщений  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> [in] Указатель на объект, для которого устанавливаются атрибуты свойств. 
    
 _lpPropTags_
  
> [in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащую массив тегов свойств, указывающих свойства, для которых устанавливаются атрибуты свойств. 
    
 _lpPropAttrs_
  
> [in] Указатель на [структуру SPropAttrArray](spropattrarray.md) с перечислением атрибутов свойства. 
    
 _lppPropProblems_
  
> [вышел] Указатель на возвращенную [структуру SPropProblemArray,](spropproblemarray.md) содержащую набор проблем свойств. Эта структура определяет проблемы, с которыми сталкиваются, если **SetAttribIMsgOnIStg** удалось установить некоторые свойства, но не все. Если указатель на NULL передается в  _параметре lppPropProblems,_ массив проблем свойств не возвращается, даже если некоторые свойства не заданы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался в целом, но один или несколько свойств не удалось получить доступ и были возвращены с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Примечания

Атрибуты свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для структурированного объекта хранения OLE, [OpenIMsgOnIStg](openimsgonistg.md) создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта **IStorage** OLE. Атрибуты свойств таких объектов можно установить или изменить с **помощью SetAttribIMsgOnIStg** и получить с [помощью GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Обратите** внимание, что **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** не работают на всех **объектах IMessage.** Они действительны только для объектов IMessage-on-IStorage, возвращенных **OpenIMsgOnIStg.**   
  
В _параметре lpPropAttrs_ число и положение атрибутов должны соответствовать числу и расположению тегов свойств, переданных в _параметре lpPropTags._ 
  
Функция **SetAttribIMsgOnIStg** используется для чтения свойств сообщений только при необходимости **схемы IMessage.** Поставщик примера магазина сообщений использует его для этой цели. Дополнительные сведения см. в [сообщении.](mapi-messages.md) 
  


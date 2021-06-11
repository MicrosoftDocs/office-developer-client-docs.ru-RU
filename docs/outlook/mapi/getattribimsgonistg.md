---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439998"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленного функцией [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики магазинов сообщений  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> [in] Указатель на **объект IMessage,** полученный из [функции OpenIMsgOnIStg.](openimsgonistg.md) 
    
 _lpPropTagArray_
  
> [in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащий массив тегов свойств, указывающих свойства, для которых необходимо получить атрибуты. 
    
 _lppPropAttrArray_
  
> [вышел] Указатель на указатель на возвращенную [структуру SPropAttrArray,](spropattrarray.md) которая содержит извлеченные атрибуты свойства. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался в целом, но один или несколько свойств не удалось получить доступ и были возвращены с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Примечания

Атрибуты свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для структурированного объекта хранения OLE, [OpenIMsgOnIStg](openimsgonistg.md) создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта **IStorage** OLE. Атрибуты свойств таких объектов можно установить или изменить с [помощью SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с **помощью GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** не работают на всех **объектах IMessage.** Они действительны только для объектов IMessage-on-IStorage, возвращенных **OpenIMsgOnIStg.**   
  
Количество и позиции атрибутов в параметре _lppPropAttrArray_ соответствуют числу и расположению тегов свойств в параметре _lpPropTagArray._ 
  


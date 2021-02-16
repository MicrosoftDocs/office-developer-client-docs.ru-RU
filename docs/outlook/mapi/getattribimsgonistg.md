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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленные функцией [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики store сообщений  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Параметры

 _lpObject_
  
> [in] Указатель на объект **IMessage,** полученный из [функции OpenIMsgOnIStg.](openimsgonistg.md) 
    
 _lpPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, указывающих свойства, для которых требуется получить атрибуты. 
    
 _lppPropAttrArray_
  
> [out] Указатель на указатель на возвращенную [структуру SPropAttrArray,](spropattrarray.md) которая содержит извлеченные атрибуты свойства. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов в целом был успешным, но не удалось получить доступ к одному или более свойствам, и он был возвращен с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Примечания

Доступ к атрибутам свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для объекта OLE структурированного хранилища, [OpenIMsgOnIStg](openimsgonistg.md) создает объект [IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта OLE **IStorage.** Атрибуты свойств для таких объектов можно установить или изменить с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с помощью **GetAttribIMsgOnIStg.** 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают не на всех **объектах IMessage.** Они действительны только для **объектов IMessage**-on-IStorage, возвращенных **OpenIMsgOnIStg.**  
  
Число и позиции атрибутов в параметре _lppPropAttrArray_ соответствуют числу и положениям тегов свойств в параметре _lpPropTagArray._ 
  


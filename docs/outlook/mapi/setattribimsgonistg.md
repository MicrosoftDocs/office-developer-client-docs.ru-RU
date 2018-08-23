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
ms.openlocfilehash: 076fb4946af9a80e53fb8452d720c22b351f5ef6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572524"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает или изменяет атрибуты свойств в объект [IMessage](imessageimapiprop.md) функцию [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики удаленного хранилища клиентских приложений и сообщения  <br/> |
   
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
  
> [in] Указатель на объект, для которых свойство задаются атрибуты. 
    
 _lpPropTags_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий массив теги свойство, определяющее, какие свойства задаются атрибуты свойства. 
    
 _lpPropAttrs_
  
> [in] Указатель на структуру [SPropAttrArray](spropattrarray.md) атрибуты свойства для установки списков. 
    
 _lppPropProblems_
  
> [out] Указатель на структуру [SPropProblemArray](spropproblemarray.md) возвращенные, содержащий набор свойств проблем. Эта структура определяет проблем, возникающих при **SetAttribIMsgOnIStg** была возможность установить некоторые свойства, но не все. Если в параметре _lppPropProblems_ передается указатель на значение NULL, массив проблема не свойство возвращается даже в том случае, если не заданы некоторые свойства. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно в целом, но одно или несколько свойств не удается получить доступ к и были возвращены с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Замечания

Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса. Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая [OpenIMsgOnIStg](openimsgonistg.md) [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** . Атрибуты свойств для таких объектов можно задать или изменены с помощью **SetAttribIMsgOnIStg** и получены с [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Примечание** **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают на все объекты **IMessage** . Они действительны только для **IMessage**- on - **IStorage** объекты, возвращаемые **OpenIMsgOnIStg**. 
  
В параметре _lpPropAttrs_ номер и положение атрибутов должны соответствовать номер и положение тегов свойств, переданной в параметре _lpPropTags_ . 
  
Функция **SetAttribIMsgOnIStg** используется для сделать свойства сообщений доступно только для чтения, при необходимости в схеме **IMessage** . Пример поставщика хранилища сообщений использует его для этой цели. [Дополнительные сведения см.](mapi-messages.md) 
  


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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ddb6d692a8e76a9c24affc3af9f612a6f1c0d769
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808532"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Применимо к**: Outlook 
  
Извлекает атрибуты свойств в объект [IMessage](imessageimapiprop.md) функцию [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики удаленного хранилища клиентских приложений и сообщения  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> [in] Указатель на объект **IMessage** , полученный из функции [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив свойств, для которых должны получить атрибуты тегов свойств. 
    
 _lppPropAttrArray_
  
> [out] Указатель на указатель на структуру возвращенные [SPropAttrArray](spropattrarray.md) , который содержит атрибуты, извлеченное свойство. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно в целом, но одно или несколько свойств не удается получить доступ к и были возвращены с типом свойства PT_ERROR.
    
## <a name="remarks"></a>Замечания

Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса. Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая [OpenIMsgOnIStg](openimsgonistg.md) [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** . Атрибуты свойств для таких объектов можно задать или изменены с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получены с **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают на все объекты **IMessage** . Они действительны только для **IMessage**- on - **IStorage** объекты, возвращаемые **OpenIMsgOnIStg**. 
  
Количество и положения атрибуты с помощью параметра _lppPropAttrArray_ соответствуют номер и положения тегов свойств с помощью параметра _lpPropTagArray_ . 
  


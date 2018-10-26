---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592375"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет альтернативный способ для вызова метода OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Параметры

 _панк_
  
> [in] Указатель на интерфейс на основе интерфейс **IUnknown** другими словами любого интерфейса MAPI. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.
    
## <a name="remarks"></a>Замечания

 **UlAddRef** возвращает значение, возвращаемое методом **IUnknown::AddRef** , который является новое значение счетчика ссылок для интерфейса. Значение не равно нулю. 
  
Дополнительные сведения о **IUnknown::AddRef**см [Интерфейс IUnknown](implementing-the-iunknown-interface.md). 
  


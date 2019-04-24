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
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315374"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет альтернативный способ вызова метода OLE **IUnknown:: AddRef**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Параметры

 _пунк_
  
> возврата Указатель на интерфейс, производный от интерфейса **IUnknown** , другими словами, любой интерфейс MAPI. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
МАПИ_Е_КАЛЛ_ФАИЛЕД 
  
> Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.
    
## <a name="remarks"></a>Замечания

 **Уладдреф** возвращает значение, возвращенное методом **IUnknown:: AddRef** , который является новым значением счетчика ссылок для интерфейса. Значение не равно нулю. 
  
Дополнительные сведения о **IUnknown:: AddRef**можно найти [в статье реализация интерфейса IUnknown](implementing-the-iunknown-interface.md). 
  


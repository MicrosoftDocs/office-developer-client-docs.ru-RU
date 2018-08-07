---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812545"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Относится к**: Outlook 
  
Предоставляет альтернативный способ для вызова метода OLE **функции IUnknown::Release**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Параметры

 _панк_
  
> [in] Указатель на интерфейс на основе интерфейс **IUnknown** другими словами любого интерфейса MAPI. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.
    
## <a name="remarks"></a>Замечания

Счетчик — число существующие указатели на элемент, который нужно освободить. 
  
Если параметр _punk_ имеет значение NULL, функция возвращает сразу же без вызова **функции IUnknown::Release**
  
 **UlRelease** возвращает значение, возвращаемое методом **функции IUnknown::Release** , который может быть равно количеству ссылку для объекта нужно освободить. 
  
Дополнительные сведения о **функции IUnknown::Release**см [Интерфейс IUnknown](implementing-the-iunknown-interface.md). 
  


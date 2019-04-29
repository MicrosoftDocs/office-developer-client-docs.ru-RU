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
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415847"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет альтернативный способ вызова метода OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlRelease(
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
    
## <a name="remarks"></a>Примечания

Число ссылок — это количество существующих указателей на освобождаемый объект. 
  
Если параметр _пунк_ имеет значение null, функция немедленно возвращает результат без вызова **IUnknown:: Release**
  
 **Улрелеасе** возвращает значение, возвращенное методом **IUnknown:: Release** , которое может равняться счетчику ссылок для освобожденного объекта. 
  
Дополнительные сведения о выПуске **IUnknown:: Release**можно найти [в статье реализация интерфейса IUnknown](implementing-the-iunknown-interface.md). 
  


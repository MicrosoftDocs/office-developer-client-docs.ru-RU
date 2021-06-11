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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет альтернативный способ вызова метода OLE **IUnknown::Release**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parameters

 _punk_
  
> [in] Указатель на интерфейс, полученный из **интерфейса IUnknown,** другими словами, любого интерфейса MAPI. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка неожиданного или неизвестного происхождения не позволяет завершить операцию.
    
## <a name="remarks"></a>Примечания

Эталонным числом является количество существующих указателей на выпущенный объект. 
  
Если параметр  _punk_ NULL, функция возвращается немедленно, не вызывая **IUnknown::Release**
  
 **UlRelease** возвращает значение, возвращенное методом **IUnknown::Release,** которое может быть равно отсчету ссылок для объекта, который будет выпущен. 
  
Дополнительные сведения об **интерфейсе IUnknown::Release** см. в выпуске [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md). 
  


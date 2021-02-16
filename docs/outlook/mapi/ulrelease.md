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
  
Предоставляет альтернативный способ вызова метода OLE **IUnknown::Release.** 
  
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

## <a name="parameters"></a>Параметры

 _1_
  
> [in] Указатель на интерфейс, производный от **интерфейса IUnknown,** другими словами, любой интерфейс MAPI. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка непредвиденного или неизвестного источника помешала выполнению операции.
    
## <a name="remarks"></a>Примечания

Количество ссылок — это количество существующих указателей на объект, который необходимо освободить. 
  
Если  _параметром parameter_ является NULL, функция немедленно возвращается без вызова **IUnknown::Release**
  
 **UlRelease** возвращает значение, возвращенное методом **IUnknown::Release,** которое может быть равно отсчету для объекта, который необходимо освободить. 
  
Дополнительные сведения о **IUnknown::Release** см. в реализации [интерфейса IUnknown.](implementing-the-iunknown-interface.md) 
  


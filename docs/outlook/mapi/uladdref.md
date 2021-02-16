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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432837"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет альтернативный способ вызова метода OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlAddRef(
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

 **UlAddRef** возвращает значение, возвращенное методом **IUnknown::AddRef,** которое является новым значением отсчета для интерфейса. Значение не являетсяzero. 
  
Дополнительные сведения об **IUnknown::AddRef** см. в окне [реализации интерфейса IUnknown.](implementing-the-iunknown-interface.md) 
  


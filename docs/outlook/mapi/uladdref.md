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
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812523"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Относится к**: Outlook 
  
Предоставляет альтернативный способ для вызова метода OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG UlAddRef(
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

 **UlAddRef** возвращает значение, возвращаемое методом **IUnknown::AddRef** , который является новое значение счетчика ссылок для интерфейса. Значение не равно нулю. 
  
Дополнительные сведения о **IUnknown::AddRef**см [Интерфейс IUnknown](implementing-the-iunknown-interface.md). 
  


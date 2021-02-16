---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428902"
---
# <a name="hrallocadvisesink"></a>HrAllocAdviseSink

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает объект-сигнальный ток с учетом контекста, заданного реализацией вызова, и функции вызова, запускаемой в уведомлении о событии. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Параметры

 _lpfnCallback_
  
> [in] Указатель на функцию вызова, основанную на прототипе [NOTIFCALLBACK,](notifcallback.md) который MAPI должен вызывать, когда происходит событие уведомления для только что созданного конвейера консультации. 
    
 _lpvContext_
  
> [in] Указатель на данные вызываемого вызова, переданные функции вызова при вызове MAPI. Данные звоняшего могут представлять адрес важности для клиента или поставщика. Обычно для кода C++ параметр  _lpvContext_ представляет указатель на адрес объекта. 
    
 _lppAdviseSink_
  
> [out] Указатель на указатель на рекомендуемый объект-тоник.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Чтобы использовать функцию **HrAllocAdviseSink,** клиентские приложения или поставщик службы создает объект для получения уведомлений, создает функцию вызова уведомления на основе прототипа функции [NOTIFCALLBACK,](notifcallback.md) который идет с этим объектом, и передает указатель на объект в функции **HrAllocAdviseSink в** качестве значения _lpvContext._ При этом выполняется уведомление; в процессе уведомления MAPI вызывает функцию вызова с указателем объекта в качестве контекста. 
  
MAPI асинхронно реализует механизм уведомлений. В C++ методом вызова уведомлений может быть объект. Если объект, который создает уведомление, не существует, клиент или поставщик, запрашивающий уведомление, должен хранить отдельное количество ссылок для этого объекта для сигнального сигнала. 
  
> [!CAUTION]
> **HrAllocAdviseSink** следует использовать экономно; Клиентам будет более безопасным создавать собственные мюникы для консультаций. 
  


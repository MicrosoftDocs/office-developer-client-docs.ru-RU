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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает объект раковины рекомендации, учитывая контекст, заданный реализацией вызовов и функцией вызова, которая будет вызвана уведомлением события. 
  
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

## <a name="parameters"></a>Parameters

 _lpfnCallback_
  
> [in] Указатель на функцию вызова на основе прототипа [NOTIFCALLBACK,](notifcallback.md) который MAPI должен вызывать при событии уведомления для вновь созданной раковины рекомендации. 
    
 _lpvContext_
  
> [in] Указатель на данные вызываемого звонка, переданные функции вызова при вызове MAPI. Данные вызываемого клиента могут представлять адрес, который имеет значение для клиента или поставщика. Как правило, для кода C++ параметр  _lpvContext_ представляет указатель на адрес объекта. 
    
 _lppAdviseSink_
  
> [вышел] Указатель на указатель на объект раковины рекомендации.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Чтобы использовать функцию **HrAllocAdviseSink,** клиентский приложение или поставщик услуг создает объект для получения уведомлений, создает функцию вызова уведомлений на основе прототипа функции [NOTIFCALLBACK,](notifcallback.md) который идет с этим объектом, и передает указатель на объект в функции **HrAllocAdviseSink** в качестве _значения lpvContext._ При этом выполняется уведомление; и в рамках процесса уведомления MAPI вызывает функцию вызова с указателем объекта в качестве контекста. 
  
MAPI асинхронно реализует свой двигатель уведомлений. В C++вызов уведомлений может быть объектным методом. Если объект, генерирующий уведомление, не присутствует, клиент или поставщик, запрашивающий уведомление, должен иметь отдельный справочный номер для этого объекта для раковины рекомендации объекта. 
  
> [!CAUTION]
> **HrAllocAdviseSink** следует использовать экономно; клиентам безопаснее создавать собственные раковины для консультирования. 
  


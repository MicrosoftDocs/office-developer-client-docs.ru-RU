---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565839"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию обратного вызова, которая вызывает MAPI, когда он может закрыть диалоговое окно безрежимным адресной книги. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Функция реализован:  <br/> |Клиентские приложения  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] От реализации значение, обычно используется для передачи в функцию сведения о пользовательском интерфейсе. Например в Microsoft Windows этот параметр является дескриптор родительского окна для диалогового окна и имеет тип HWND, привести к **ULONG_PTR**. Нулевое значение указывает, что нет родительского окна. 
    
 _lpvContext_
  
> [in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI. Это значение может представлять адрес важности для клиентского приложения. Обычно для кода C++ _lpvContext_ — это указатель на адрес экземпляр объекта C++. 
    
## <a name="return-value"></a>Возвращаемое значение

Отсутствует
  
## <a name="remarks"></a>Замечания

Когда клиентское приложение вызывает диалоговое окно безрежимным адресной книги, он содержит в цикл сообщений Windows вызов функции, основанной на прототип [ACCELERATEABSDI](accelerateabsdi.md) , которая проверяет и обрабатывает сочетания клавиш. При закрытии диалоговое окно вызовов MAPI с **DISMISSMODELESS** на основе функции, чтобы клиентское приложение остановит вызов **ACCELERATEABSDI** на основе функции. 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)


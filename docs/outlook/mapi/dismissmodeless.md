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
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428188"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию callback, которую MAPI вызывает, когда она отклонять диалоговое окно адресной книги без режима. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Клиентские приложения  <br/> |
|Определяемая функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Значение, специфичная для реализации, обычно используется для передачи сведений пользовательского интерфейса в функцию. Например, в Microsoft Windows этот параметр является родительским окне для диалоговых окон и имеет тип HWND, приведите его **к** ULONG_PTR . Нулевое значение указывает, что родительского окна нет. 
    
 _lpvContext_
  
> [in] Указатель на произвольное значение, передав его функции вызова при вызове MAPI. Это значение может представлять адрес важности для клиентского приложения. Как правило, для кода C++  _lpvContext_ — это указатель на адрес экземпляра объекта C++. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет
  
## <a name="remarks"></a>Примечания

Когда клиентская приложение вызывает диалоговое окно без режима адресной книги, оно включает в цикл сообщений Windows вызов функции на основе прототипа [ACCELERATEABSDI,](accelerateabsdi.md) который проверяет и обрабатывает ускорители клавиш. Когда диалоговое окно закрыто, MAPI вызывает функцию на основе **DISMISSMODELESS,** чтобы клиентские приложения перестали вызывать функцию на основе **ACCELERATEABSDI.** 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)


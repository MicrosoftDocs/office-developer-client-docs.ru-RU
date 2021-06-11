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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, вызываемую MAPI при отклонении диалогового окна без режима адресной книги. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Клиентские приложения  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Значение, определенное для реализации, обычно используется для передачи сведений об пользовательском интерфейсе в функцию. Например, в Microsoft Windows этот параметр является родительской ручкой окна для диалогового окна и имеет тип HWND, отбрасыв в **ULONG_PTR.** Значение нуля указывает на отсутствие родительского окна. 
    
 _lpvContext_
  
> [in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI. Это значение может представлять адрес значения для клиентского приложения. Как правило, для кода C++  _lpvContext_ является указателем на адрес экземпляра объекта C++. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет
  
## <a name="remarks"></a>Примечания

Когда клиентская заявка вызывает диалоговое окно без режима адресной книги, оно включает в цикл Windows сообщения вызов функции на основе прототипа [ACCELERATEABSDI,](accelerateabsdi.md) который проверяет и обрабатывает клавиши акселератора. Когда диалоговое окно закрыто, MAPI вызывает основанную **на DISMISSMODELESS** функцию, чтобы клиентские приложения перестали вызывать функцию **ACCELERATEABSDI.** 
  
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)


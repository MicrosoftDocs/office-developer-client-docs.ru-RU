---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420376"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова для обработки клавиш акселератора в диалоговом окне без режима адресной книги. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определенные функции, реализованные в:  <br/> |MAPI  <br/> |
|Определенная функция, вызванная:  <br/> |Клиентские приложения  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Значение, определенное для реализации, используемого для передачи данных пользовательского интерфейса функции. В приложениях, работающих в Microsoft Windows, _ulUIParam_ является родительской ручкой окна для диалоговой окне и имеет тип HWND, отбрасыв в **ULONG_PTR**. Значение нуля указывает на отсутствие родительского окна. 
    
 _lpvmsg_
  
> [in] Указатель на сообщение Windows.
    
## <a name="return-value"></a>Возвращаемое значение

Функция с **прототипом ACCELERATEABSDI** возвращает TRUE, если она обрабатывает сообщение. 
  
## <a name="remarks"></a>Примечания

Функция, основанная на прототипе **ACCELERATEABSDI,** используется только с бес режимным диалогом, то есть только в том случае, если клиентская заявка задает флаг DIALOG_SDI в члене _ulFlags_ структуры [ADRPARM.](adrparm.md) 
  
Бесхимный диалоговое окно делится циклом сообщений Windows клиентского приложения, а не собственным циклом. Приложение, которое управляет циклом сообщений, не знает, какие клавиши акселератора использует диалоговое окно, поэтому оно вызывает функцию **ACCELERATEABSDI,** чтобы проверить и действовать на клавишах акселератора, таких как CTRL+P для печати. 
  
Цикл сообщений клиента вызывает функцию **ACCELERATEABSDI,** когда клиент вызывает диалоговое окно без режима адресной книги с методом [IAddrBook::Address.](iaddrbook-address.md) Этот вызов прекращается, когда MAPI вызывает функцию на основе прототипа [функции DISMISSMODELESS.](dismissmodeless.md) 
  


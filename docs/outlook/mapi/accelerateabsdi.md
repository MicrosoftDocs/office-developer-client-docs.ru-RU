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
ms.openlocfilehash: 101e74f3e35e3664dd29e59f166b2f0af6e1dcba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592040"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию обратного вызова для процесса сочетания клавиш в диалоговом окне безрежимным адресная книга. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Функция реализован:  <br/> |MAPI  <br/> |
|Вызывается функция:  <br/> |Клиентские приложения  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] От реализации значение, используемое для передачи сведения о пользовательском интерфейсе функции. В приложениях, использующих на Microsoft Windows _ulUIParam_ является дескриптор родительского окна для диалогового окна и типа HWND, привести к **ULONG_PTR**. Нулевое значение указывает, что нет родительского окна. 
    
 _lpvmsg_
  
> [in] Указатель на сообщение Windows.
    
## <a name="return-value"></a>Возвращаемое значение

Функция с прототип **ACCELERATEABSDI** возвращает TRUE, если он обрабатывает сообщение. 
  
## <a name="remarks"></a>Замечания

Функции, основанной на прототип **ACCELERATEABSDI** используется только с безрежимным диалоговое окно, то есть только в том случае, если клиентское приложение значение флага DIALOG_SDI в член _ulFlags_ структуры [ADRPARM](adrparm.md) . 
  
Безрежимные диалоговое окно общего клиентского приложения Windows цикл обработки сообщений, а не через собственный цикл обработки. Приложения, который управляет цикл обработки сообщений, не знать, какие сочетания клавиш, используется диалоговое окно, поэтому он вызывает **ACCELERATEABSDI** на основе функцию, чтобы проверить, а также для выполнения сочетания клавиш, например CTRL + P для печати. 
  
Вызовы цикла сообщений клиента **ACCELERATEABSDI** на основе функции, когда клиент вызывает диалоговое окно безрежимным адресной книги с помощью метода [IAddrBook::Address](iaddrbook-address.md) . Этот вызов будет завершен при MAPI вызывает функцию на основании прототипа функции [DISMISSMODELESS](dismissmodeless.md) . 
  


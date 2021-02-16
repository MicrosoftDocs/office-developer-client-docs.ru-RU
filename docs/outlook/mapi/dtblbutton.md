---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412788"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения об кнопке для диалоговых окна, построенных из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанный макрос:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>"Участники"

 **ulbLpszLabel**
  
> Положение в памяти строки символов, отображаемой на кнопке.
    
 **ulFlags**
  
> Битовая метка флагов, используемая для обозначения формата метки, на который указывает элемент **ulbLpszLabel.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.
    
 **ulPRControl**
  
> Тег свойства для свойства типа PT_OBJECT, который реализует [интерфейс IMAPIControl.](imapicontroliunknown.md) При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) таблицы отображения, чтобы получить это свойство. 
    
## <a name="remarks"></a>Примечания

Структура **DTBLBUTTON** описывает кнопку, которая позволяет пользователю при нажатии на нее начать операцию. Обычно при нажатии кнопки отображается модальные диалоговые окна или вызывается программная задача. Поставщики услуг могут реализовать что угодно с помощью кнопки. Если кнопка должна выполнять задачу на основе значений других элементов управления, эти элементы управления должны установить флаг DT_SET_IMMEDIATE элементов управления. 
  
Член **ulbLpszLabel** — это положение в памяти строки символов, отображаемой на кнопке. Поставщики услуг могут добавить символ амперанд ( ) для обозначения &amp; ускорителя Windows в метку кнопки. Нажатие клавиши ускорителя имеет тот же эффект, что и нажатие кнопки. 
  
Член **ulPRControl** описывает свойство объекта, которое при открытом методе **IMAPIProp::OpenProperty** возвращает указатель на объект управления. Реализация объекта управления, который поддерживает интерфейс **IMAPIControl,** позволяет расширить набор функций MAPI и определить операцию или задачу, которая выполняется при нажатии кнопки. **IMAPIControl** обеспечивает два метода управления кнопками: [GetState](imapicontrol-getstate.md) для отключения или включения кнопок и активации для обработки нажатий кнопок. [](imapicontrol-activate.md) 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


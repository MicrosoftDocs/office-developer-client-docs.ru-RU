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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о том, как управлять кнопками для диалогового окна, построенного из таблицы отображения.
  
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
  
> Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabel.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.
    
 **ulPRControl**
  
> Тег свойства для свойства типа PT_OBJECT, реализуемого [интерфейсом IMAPIControl.](imapicontroliunknown.md) При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) таблицы отображения для получения этого свойства. 
    
## <a name="remarks"></a>Примечания

Структура **DTBLBUTTON** описывает кнопку управления, которая при нажатии позволяет пользователю приступить к операции. Как правило, при нажатии кнопки отображается диалоговое окно modal или вызывается программатическая задача. Поставщики услуг могут реализовать все, что угодно с помощью кнопки управления. Если предполагается, что кнопка выполняет задачу на основе значений других элементов управления, эти элементы управления должны установить флаг DT_SET_IMMEDIATE. 
  
Член **ulbLpszLabel** — это положение в памяти строки символов, отображаемой на кнопке. Поставщики услуг могут добавить символ ampersand () для обозначения Windows &amp; ускорителя на мете кнопки. Нажатие клавиши акселератора имеет тот же эффект, что и нажатие кнопки. 
  
Участник **ulPRControl** описывает свойство объекта, которое при открытом методе **IMAPIProp::OpenProperty** возвращает указатель на объект управления. Реализация объекта управления, который поддерживает интерфейс **IMAPIControl,** позволяет расширить набор функций MAPI и определить операцию или задачу, которая возникает при нажатии кнопки. **IMAPIControl** обеспечивает два метода управления кнопками: [GetState](imapicontrol-getstate.md) для отключения или включения кнопок и активации для обработки нажатий кнопки. [](imapicontrol-activate.md) 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


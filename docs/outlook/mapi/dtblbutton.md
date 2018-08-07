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
ms.openlocfilehash: 2505f555fd8867fdc24a14f523a74b6f478a3e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808352"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Относится к**: Outlook 
  
Содержит сведения об элементе управления кнопки для диалогового окна, построенная на основе таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Положение в памяти строки символ, отображаемый на кнопке.
    
 **ulFlags**
  
> Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.
    
 **ulPRControl**
  
> Свойство tag для свойства типа PT_OBJECT, который реализует интерфейс [IMAPIControl](imapicontroliunknown.md) . При нажатии кнопки MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для реализации [IMAPIProp](imapipropiunknown.md) отображения таблицы для получения этого свойства. 
    
## <a name="remarks"></a>Замечания

Структура **DTBLBUTTON** описывает элемент управления кнопка, при нажатии этой кнопки, позволяющее начала операции. Как правило нажав кнопку вызывает модального диалогового окна для отображения или программные задачи для вызова. Поставщиков услуг можно реализовать все действия через элемент управления button. Если предполагается, что кнопки выполнения определенной задачи, на основе значений других элементов управления, эти элементы управления должны иметь флаг DT_SET_IMMEDIATE. 
  
Член **ulbLpszLabel** является позицию в памяти строки символ, отображаемый на кнопке. Поставщиков услуг можно добавить амперсанда (&amp;) для указания ускорителя Windows в метки кнопки. Нажав сочетание клавиш имеет тот же эффект, как нажатие кнопки. 
  
Член **ulPRControl** описывает свойства объекта, который, при открытии с помощью метода **IMAPIProp::OpenProperty** возвращает указатель на объект элемента управления. Реализация объект элемента управления, который поддерживает интерфейс **IMAPIControl** — это способ расширить набор компонентов MAPI и определить операции или задачи, что происходит при нажатии кнопки. **IMAPIControl** предоставляет два методы для работы с кнопками: [GetState](imapicontrol-getstate.md) , чтобы отключить или включить кнопки и [активировать](imapicontrol-activate.md) для обработки нажатий кнопок. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


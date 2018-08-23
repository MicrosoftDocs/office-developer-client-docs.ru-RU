---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569766"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> Битовая маска флаги, используемые для устранения полосу прокрутки горизонтальный или вертикальный из списка. Можно задать следующие флажки:
    
MAPI_NO_HBAR 
  
> В списке должны быть отображены горизонтальной полосы прокрутки.
    
MAPI_NO_VBAR 
  
> Не вертикальная полоса прокрутки, отображаемые в списке.
    
 **ulPRSetProperty**
  
> Свойство tag для свойства любого типа. Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Тег свойства для свойства в таблице типа PT_OBJECT, которая может быть открыта с помощью **OpenProperty** вызова. Число столбцов, которые должны иметь таблицы зависит от того, является ли список выделение одного или нескольких элементов списка. Если член **ulPRSetProperty** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), списке обеспечивает несколько фрагментов.
    
## <a name="remarks"></a>Замечания

Структура **DTBLLBX** описывает элемент управления, который используется для отображения нескольких элементов и позволяют пользователю выбрать одну или несколько элементов списка. 
  
**UlPRSetProperty** , а **ulPRTableName** работать вместе; При выборе одного значения из таблицы, он записывается обратно в **ulPRSetProperty** при диалоговое окно закрывается. 
  
Значение флагов указывает, следует ли отображать полосы прокрутки горизонтальный или вертикальный со списком. Значение по умолчанию — иметь типы прокрутки полосы отображаются, если это необходимо. Поставщиков услуг можно задать MAPI_NO_HBAR для отмены вывода горизонтальной полосы прокрутки и MAPI_NO_VBAR для отмены вывода вертикальной полосы прокрутки. 
  
Элементы тега два свойства работают вместе для отображения значений в списке соответствующих свойств при выборе элемента в списке. Когда MAPI сначала отображается список, вызывает метод **OpenProperty** реализации **IMAPIProp** для получения таблицы, обнаруженных в элементе **ulPRTableName** . Количество столбцов в таблице определяется значение элемента **ulPRSetProperty** . Если **ulPRSetProperty** **PR_NULL**, список, несколько список выбора, основанный на объект, который содержит получателей, например контейнер адресной книги, таблице получателей сообщения или таблицу содержимого списка рассылки. 
  
Таблица для нескольких список выбора должен включать следующие столбцы:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) и с тремя обязательные столбцы также может отображаться не более пяти другие свойства многозначных строковых. 
  
Если член **ulPRSetProperty** установлено значение **PR_NULL**, список, список выбора одного элемента. Начальное значение **ulPRSetProperty** определяет первой выбранной строки. При выборе одной из строк, — это набор элементов **ulPRSetProperty** на выбранное значение и это значение записывается обратно в реализации интерфейса свойства с помощью вызова [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


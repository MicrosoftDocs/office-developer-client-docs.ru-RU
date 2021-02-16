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
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438570"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает список, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
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

## <a name="members"></a>Элементы

 **ulFlags**
  
> Битоваяmas флагов, используемая для устранения горизонтальной или вертикальной полоса прокрутки в списке. Можно установить следующие флаги:
    
MAPI_NO_HBAR 
  
> Горизонтальная полоса прокрутки не должна быть показана вместе со списком.
    
MAPI_NO_VBAR 
  
> Вертикальная лямка прокрутки не должна быть показана вместе со списком.
    
 **ulPRSetProperty**
  
> Тег свойства для свойства любого типа. Это свойство является одним из столбцов в таблице, заданной членом **ulPRTableTable.** 
    
 **ulPRTableName**
  
> Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью вызова **OpenProperty.** Число столбцов в таблице зависит от того, является ли список одним или нескольким списком выбора. Если для **члена ulPRSetProperty** установлено PR_NULL **(** [PidTagNull),](pidtagnull-canonical-property.md)список позволяет выбрать несколько вариантов.
    
## <a name="remarks"></a>Примечания

Структура **DTBLLBX** описывает список элементов управления, используемых для показа нескольких элементов и позволяя пользователю выбрать один или несколько элементов. 
  
Члены **ulPRSetProperty** и **ulPRTableName** работают вместе; Если в таблице выбрано одно значение, оно возвращается в **ulPRSetProperty,** когда диалоговое окно будет отклонено. 
  
Значение флагов указывает, должна ли отображаться горизонтальная или вертикальная полоса прокрутки со списком. По умолчанию типы полос прокрутки отображаются, если это необходимо. Поставщики услуг могут настроить MAPI_NO_HBAR подавления горизонтальной полоса прокрутки и MAPI_NO_VBAR для подавления вертикальной полоса прокрутки. 
  
Два элемента тега свойства совместно отображают значения в списке и устанавливают соответствующие свойства при выборе элемента в списке. При первом отображении списка MAPI вызывает метод **OpenProperty** реализации **IMAPIProp** для получения таблицы, определенной в члене **ulPRTableName.** Количество столбцов в таблице зависит от значения члена **ulPRSetProperty.** Если **для ulPRSetProperty** установлено **PR_NULL,** список является списком выбора нескольких объектов, основанных на объекте, который содержит получателей, таких как контейнер адресной книги, таблица получателей для сообщения или таблица содержимого списка рассылки. 
  
Таблица для нескольких списков выбора должна включать следующие столбцы:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
  
 **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)и не более пяти других многоценных свойств строки также могут отображаться с тремя требуми столбцами. 
  
Если для **члена ulPRSetProperty** не установлено **PR_NULL,** список является одним списком выбора. Начальное значение **ulPRSetProperty** определяет первую выбранную строку. Когда пользователь выбирает одну из строк, для члена **ulPRSetProperty** устанавливается выбранное значение, и это значение записуется обратно в реализацию интерфейса свойства с вызовом [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


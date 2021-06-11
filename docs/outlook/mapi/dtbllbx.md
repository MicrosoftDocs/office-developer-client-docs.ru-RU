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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
  
> Bitmask флагов, используемых для устранения горизонтальной или вертикальной панели прокрутки из списка. Можно установить следующие флаги:
    
MAPI_NO_HBAR 
  
> В списке не следует показывать горизонтальную полосу прокрутки.
    
MAPI_NO_VBAR 
  
> В списке не следует показывать вертикальную планку прокрутки.
    
 **ulPRSetProperty**
  
> Тег свойства для свойства любого типа. Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableTable.** 
    
 **ulPRTableName**
  
> Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью **вызова OpenProperty.** Количество столбцов, которые должны иметься в таблице, зависит от того, является ли список одним или нескольким списком выбора. Если для **члена ulPRSetProperty** установлено PR_NULL [(PidTagNull),](pidtagnull-canonical-property.md)в списке допускается несколько вариантов выбора. 
    
## <a name="remarks"></a>Примечания

Структура **DTBLLBX** описывает список элементов управления, используемых для показа нескольких элементов, и позволит пользователю выбрать один или несколько элементов. 
  
Член **ulPRSetProperty** и **член ulPRTableName** работают вместе; Когда из таблицы выбирается одно значение, оно возвращается в **ulPRSetProperty** при отклонении диалоговое окно. 
  
Значение флагов указывает, следует ли отображать в списке горизонтальную или вертикальную полосу прокрутки. По умолчанию должны отображаться типы слитков прокрутки, если это необходимо. Поставщики услуг могут MAPI_NO_HBAR для подавления горизонтальной панели прокрутки и MAPI_NO_VBAR для подавления вертикальной панели прокрутки. 
  
Два элемента тега свойств работают вместе, чтобы отображать значения в списке и устанавливать соответствующие свойства при выборе элемента в списке. Когда MAPI впервые отображает список, он вызывает метод **реализации IMAPIProperty** для получения таблицы, определенной в члене **ulPRTableName.**  Количество столбцов в таблице зависит от значения участника **ulPRSetProperty.** Если **для ulPRSetProperty** установлено **PR_NULL,** список — это несколько списков выбора, основанных на объекте, который содержит получателей, таких как контейнер адресной книги, таблица получателей для сообщения или таблица контента списка рассылки. 
  
Таблица для нескольких списков выбора должна включать следующие столбцы:
  
 **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
  
 **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
  
 **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
  
 **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)и не более пяти других многоценных свойств строк можно также отображать с помощью трех необходимых столбцов. 
  
Если у **члена ulPRSetProperty** не установлено **PR_NULL,** список является единым списком выбора. Начальное значение **ulPRSetProperty** определяет первую выбранную строку. Когда пользователь выбирает одну из строк, член **ulPRSetProperty** заданной для выбранного значения, и это значение возвращается в реализацию интерфейса свойств с вызовом [на IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


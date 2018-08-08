---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808341"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Относится к**: Outlook 
  
Содержит сведения о флажок, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Положение в памяти строку символов, которое будет отображаться с флажок. 
    
 **ulFlags**
  
> Битовая маска флаги используется для назначения формат метки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.
    
 **ulPRPropertyName**
  
> Свойство tag для свойства типа PT_BOOLEAN. Значение этого свойства зависит от состояния флажка.
    
## <a name="remarks"></a>Замечания

Структура **DTBLCHECKBOX** описывает флажок элемент управления, который отражает один из двух режимов: (флажком) включены или отключены (пустые поля). 
  
Член **ulPRPropertyName** описывает логическое свойство, значение которого управляется изменение состояния флажка. При первом отображении флажок MAPI вызывает метод **GetProps** реализации **IMAPIProp** , связанный с таблицей отображения для получения набора свойств по умолчанию. Если одно из свойств соответствует тег свойства в структуре **DTBLCHECKBOX** , значение для этого свойства отображается в поле проверить начальное значение. 
  
Элементы управления "флажок" можно изменить. Это позволяет пользователю изменять их состояния. Можно изменить флажки установить флаг DT_EDITABLE в **ulCtlFlags** членом их [DTCTL](dtctl.md) структуры и их свойства **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). При изменении его состояния флажка MAPI вызывает [IMAPIProp::SetProps](imapiprop-setprops.md) для свойства, определенный в член тега свойства структуры **DTBLCHECKBOX** новое состояние. 
  
К примеру поставщика адресных книг могут содержать элемент управления можно изменить флажок в диалоговое окно настройки его настроить свойство **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) получателя. Когда пользователь выбирает этот флажок, MAPI задает это свойство в значение TRUE. Если флажок не выбран, свойство имеет значение FALSE.
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см. Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)


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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436834"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения об установленном флажке, который будет использоваться в диалоговом окне, созданном из таблицы отображения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанный макрос:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>"Участники"

 **улблпсзлабел**
  
> Позиция в памяти строки символов, которая отображается вместе с флажком. 
    
 **ulFlags**
  
> Битовая маска флагов, используемых для обозначения формата метки флажка. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка имеет формат ANSI.
    
 **улпрпропертинаме**
  
> Тег свойства для свойства типа PT_BOOLEAN. Значение этого свойства зависит от состояния флажка.
    
## <a name="remarks"></a>Примечания

Структура **дтблчеккбокс** описывает флажок элемента управления, который отражает одно из двух состояний: включено (отмечено флажком) или Disabled (пустое поле). 
  
Элемент **улпрпропертинаме** описывает свойство Boolean, значение которого изменяется при изменении состояния флажка. При первом отображении этого флажка MAPI вызывает метод **PROPS** реализации **IMAPIProp** , связанной с таблицей отображения, для получения набора свойств по умолчанию. Если одно из свойств сопоставлено с тегом свойства в структуре **дтблчеккбокс** , значение этого свойства отображается в качестве начального значения флажка. 
  
Элементы управления "флажок" могут быть изменяемыми. Это позволяет пользователю изменять свои состояния. Изменяемые флажки установите флаг DT_EDITABLE в элементе **улктлфлагс** структуры [дтктл](dtctl.md) и в их свойстве **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Когда флажок изменит свое состояние, MAPI вызывает [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать свойство, указанное в элементе тега свойства в структуре **дтблчеккбокс** , в новое состояние. 
  
Например, поставщик адресной книги может содержать изменяемый элемент управления "флажок" в диалоговом окне настройки, чтобы настроить значение свойства **PR_SEND_RICH_INFO** получателя ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Когда пользователь устанавливает этот флажок, MAPI устанавливает для этого свойства значение TRUE. Если этот флажок не установлен, свойству присваивается значение FALSE.
  
Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md). Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md). Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)


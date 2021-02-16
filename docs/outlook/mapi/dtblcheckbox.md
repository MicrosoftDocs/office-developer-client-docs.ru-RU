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
  
Содержит сведения о поле, которое будет использоваться в диалоговом окне, построенного из таблицы отображения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
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

 **ulbLpszLabel**
  
> Положение в памяти строки символов, отображаемой с помощью этого контрольного окна. 
    
 **ulFlags**
  
> Битовая метка флагов, используемая для обозначения формата метки флажка. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.
    
 **ulPRPropertyName**
  
> Тег свойства для свойства типа PT_BOOLEAN. На значение этого свойства влияет состояние этого контрольного окна.
    
## <a name="remarks"></a>Примечания

В **структуре DTBLCHECKBOX** описаны контрольные очки, отражающие одно из двух состояния: включено (включено (поле) или отключено (пустое поле). 
  
Член **ulPRPropertyName** описывает boolean свойство, значение которого изменяется путем изменения состояния этого контрольного окна. При первом отображению этого окна MAPI вызывает метод **GetProps** реализации **IMAPIProp,** связанный с таблицей отображения, для получения набора свойств по умолчанию. Если одно из свойств сопомечается с тегом свойства в структуре **DTBLCHECKBOX,** значение этого свойства отображается в качестве начального значения для этого значения. 
  
Элементы управления для этого можно модификировать. Это позволяет пользователю изменять свое состояния. Модификируемые флажки устанавливают флаг DT_EDITABLE в члене **ulCtlFlags** их [структуры DTCTL](dtctl.md) и в свойстве **PR_CONTROL_FLAGS** ([PidTagControlFlags).](pidtagcontrolflags-canonical-property.md) Когда состояние установленного в этом поле изменяется, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить для свойства, обнаруженного в члене тега свойства структуры **DTBLCHECKBOX,** новое состояние. 
  
Например, поставщик адресной книги может включить в диалоговое окно конфигурации изменимый контрольный список, чтобы настроить параметр свойства PR_SEND_RICH_INFO **получателя** ([PidTagSendRichInfo).](pidtagsendrichinfo-canonical-property.md) Когда пользователь устанавливает этот контроль, MAPI устанавливает для этого свойства true. Если этот установлен, для свойства устанавливается false.
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md) Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)


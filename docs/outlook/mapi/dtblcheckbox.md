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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о поле, которое будет использоваться в диалоговом окне, построенной из таблицы отображения. 
  
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
  
> Положение в памяти строки символов, отображаемой с помощью контрольного окна. 
    
 **ulFlags**
  
> Bitmask флагов, используемых для обозначения формата метки флажка. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Метка находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.
    
 **ulPRPropertyName**
  
> Тег свойства для свойства типа PT_BOOLEAN. На значение этого свойства влияет состояние контрольного окна.
    
## <a name="remarks"></a>Примечания

Структура **DTBLCHECKBOX** описывает контрольное окно, которое отражает одно из двух штатов: включено (контрольное поле) или отключено (пустое поле). 
  
Участник **ulPRPropertyName** описывает свойство Boolean, значение которого управляется изменением состояния контрольного окна. При первом отображке контрольного окна MAPI вызывает метод **GetProps** реализации **IMAPIProp,** связанный со таблицей отображения, чтобы получить набор свойств по умолчанию. Если одно из свойств отображает тег свойства в структуре **DTBLCHECKBOX,** значение для этого свойства отображается в качестве начального значения контрольного окна. 
  
Элементы управления контрольными окнами можно модификировать. Это позволяет пользователю изменять свои состояния. Флажки модификата устанавливают флаг DT_EDITABLE в **члене ulCtlFlags** их [структуры DTCTL](dtctl.md) **и** в свойстве [PR_CONTROL_FLAGS (PidTagControlFlags).](pidtagcontrolflags-canonical-property.md) При изменениях состояния почтового ящика MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить свойство, идентифицированное в члене тега свойств структуры **DTBLCHECKBOX,** в новое состояние. 
  
Например, поставщик адресных книг может включить в диалоговое окно конфигурации управление изменяемым контрольным окном для настройки параметра свойства[PR_SEND_RICH_INFO (PidTagSendRichInfo).](pidtagsendrichinfo-canonical-property.md)  Когда пользователь выбирает контрольный ящик, MAPI задает это свойство true. При отсеклении контрольного окна свойство настроено на FALSE.
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md) Сведения о типах свойств см. в [обзоре типов свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)


---
title: Каноническое свойство PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430884"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Каноническое свойство PidTagControlFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битмаску флагов, регулирующих поведение управления, используемого в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3F00  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Для этого свойства можно установить один или несколько следующих флагов:
  
DT_ACCEPT_DBCS 
  
> Управление может иметь Double-Byte символы набора символов (DBCS). Этот флаг используется с помощью элементов управления редактирования. Он позволяет наборы символов с несколькими пойтами.
    
DT_EDITABLE 
  
> Управление может быть изменено; значение, связанное с управлением, может быть изменено. Если этот флаг не установлен, управление только для чтения. Это значение игнорируется на метке, групповом окне, стандартном нажатии кнопки, многоценном элементе управления списком и элементов управления полем списка.
    
DT_MULTILINE 
  
> Управление редактированием может содержать несколько строк. Это означает, что возвращаемая символка может быть введена в пределах управления. Этот флаг действителен только для редактирования элементов управления.
    
DT_PASSWORD_EDIT 
  
> Применяется для изменения элементов управления. Управление изменением рассматривается как пароль. Значение отображается с помощью звездочек вместо того, чтобы вторить фактические вступив символы.
    
DT_REQUIRED 
  
> Если управление позволяет вносить изменения (DT_EDITABLE), оно должно иметь значение до того, как [будет вызвано значение IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
DT_SET_IMMEDIATE 
  
> Включает немедленную настройку значения; Как только значение в области управления меняется, MAPI вызывает метод **SetProps** для свойства, связанного с этим управлением. Если этот флаг не установлен, значения устанавливаются при отклонении диалогового окна. 
    
DT_SET_SELECTION 
  
> При выборе в поле списка столбец индекса этого списка засмеяется как свойство. Всегда используется с DT_SET_IMMEDIATE.
    
Это свойство хранится в члене ulCtlFlags структуры [DTCTL](dtctl.md) управления. Большинство флагов управления применяются к всем средствам управления, которые позволяют вводить пользователя; некоторые применяются только к контролю редактирования. Элементы управления, которые не позволяют вводить пользователю, например кнопку или метку, устанавливают 0 для флагов управления. 
  
Многие значения флага являются самоопроверятельными. Например, если DT_REQUIRED для управления, оно должно содержать значение, прежде чем диалоговое окно будет разрешено отклонять. Либо поставщик услуг может предоставить значение через реализацию **IMAPIProp,** либо пользователь может ввести его. DT_EDITABLE указывает, что значение для управления может быть изменено. DT_MULTILINE позволяет значению для управления редактированием охватывать несколько строк. 
  
Некоторые флаги управления не столь очевидны в их значении. Когда управление задает флаг DT_SET_IMMEDIATE, любые изменения в его значении влияют, как только пользователь переходит на новый контроль. MAPI делает один вызов в метод [IMAPIProp::SetProps](imapiprop-setprops.md) интерфейса свойства управления. Это отличается от поведения по умолчанию, которое состоит в том, чтобы отложить внесение изменений в значения управления до тех пор, пока пользователь не выберет кнопку **ОК** или не отклонять диалоговое окно. Флаг DT_SET_IMMEDIATE часто используется в сочетании с уведомлениями таблицы отображения. 
  
В следующей таблице перечислены типы элементов управления и все значения флага, которые можно установить для каждого типа.
  
|**Control**|**Допустимые значения для этого свойства**|
|:-----|:-----|
|Кнопка  <br/> |Должно быть нулевой  <br/> |
|Флажок  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Поле со списком  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Drop-down list box  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Редактирование  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Поле группы  <br/> |Должно быть нулевой  <br/> |
|Выбор метки  <br/> |Должно быть нулевой  <br/> |
|Поле со списком  <br/> |Должно быть нулевой  <br/> |
|Multivalue drop-down list box  <br/> |Должно быть нулевой  <br/> |
|Поле "Многоценный список"  <br/> |Должно быть нулевой  <br/> |
|Страница Tabbed  <br/> |Должно быть нулевой  <br/> |
|Кнопка "Радио"  <br/> |Должно быть нулевой  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


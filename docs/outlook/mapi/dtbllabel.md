---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410688"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает метку, которая будет использоваться в диалоговом окне, построенной из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанный макрос  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>"Участники"

 **ulbLpszLabelName**
  
> Положение в памяти метки строки символов.
    
 **ulFlags**
  
> Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabelName.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.
    
## <a name="remarks"></a>Примечания

Структура **DTBLLABEL** описывает текст управления меткой, отображаемый с другим типом управления, чтобы добавить значение к этому контролю. Например, большинство элементов управления редактированием находятся рядом с метами, чтобы информировать пользователя о типе вступаемой информации. Некоторые элементы управления, такие как групповые ящики и кнопки радиосвязи, удерживают собственные метки. 
  
Метка может включать ускоритель Windows, идентифицированный в качестве символа, следующего за ampersand ( &amp; ). При нажатии клавиши акселератора фокусируется в первом элементе управления nonlabel, nonbutton после этого метки в таблице отображения.
  
Поддержка многолинейных меток не поддерживается. Отображение нескольких строк требует нескольких меток.
  
Невозможно использовать метку для редактирования только для чтения. Разница заключается в том, что управление редактированием можно выбрать и скопировать, а метка — нет. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


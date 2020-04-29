---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438395"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает элемент управления "Группа", который будет использоваться в диалоговом окне, созданном из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанный макрос:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>"Участники"

 **улблпсзлабел**
  
> Позиция в памяти строки символов, сопровождающей поле группы. Если отображается, метка отображается в верхней части поля слева.
    
 **ulFlags**
  
> Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабел** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка имеет формат ANSI.
    
## <a name="remarks"></a>Примечания

Структура **дтблграупбокс** описывает элемент управления "Группа", который используется для визуального связывания других элементов управления в диалоговом окне. Метод выделения включает окружающие другие элементы управления полем. 
  
Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md). Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)


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
  
Описание группового окна, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанный макрос:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>"Участники"

 **ulbLpszLabel**
  
> Положение в памяти строки символа, которая сопровождает поле группы. Если она отображается, метка отображается в верхней левой части окна.
    
 **ulFlags**
  
> Битовая метка флагов, используемая для обозначения формата метки, на который указывает элемент **ulbLpszLabel.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.
    
## <a name="remarks"></a>Примечания

Структура **DTBLGROUPBOX** описывает элемент управления "Групповое поле", используемый для визуального связываия других элементов управления в диалоговом окне. Метод выделения включает в себя окружение других элементов управления полем. 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

